# gm - Game Keyboard WebView Android App

## 项目简介

这是一个实验性的 Android 应用程序，旨在为特定的网页游戏提供一个自定义的屏幕虚拟键盘。项目的核心目的是解决在没有连接实体键盘的 Android 设备上，无法通过常规方式（如系统自带软键盘）向依赖实体键盘输入的网页游戏发送控制命令的问题。

应用通过嵌入 Android 的 `WebView` 组件加载网页游戏，并在界面底部显示一个自定义的虚拟键盘。通过点击这些虚拟按键，应用试图向网页注入 JavaScript 代码来模拟实体键盘的按键事件（如 `keydown`, `keyup`），从而控制游戏。

## 功能特性

*   使用 `WebView` 加载指定或用户输入的网页 URL。
*   自定义设计的屏幕虚拟键盘布局（目前包含示例按键）。
*   初步实现（骨架代码）虚拟按键点击事件处理。
*   初步实现（概念性 placeholder）通过 JavaScript 注入模拟按键事件。
*   配置了 GitHub Actions 工作流程，在代码提交时自动构建 debug APK。

## 当前状态

这是项目的初始提交，包含了标准的 Android Studio 项目结构、基础的布局文件 (`activity_main.xml`) 和 `MainActivity` 的骨架代码。

*   `WebView` 的初始化和 URL 加载已基本设置。
*   虚拟键盘的 UI 元素已在布局中定义。
*   虚拟按键的点击监听器已连接到占位符方法。
*   核心的按键事件模拟逻辑 (`simulateKeyPress` 方法中的 JavaScript 注入部分) 仍是概念性的，需要进一步的实现、测试和调试，以确保能够可靠地被目标游戏网页接收和解释。

项目的 GitHub Actions 工作流程已配置完成，每次 push 到 main 分支都会尝试构建 debug APK。

## 如何构建和运行

### 前提条件

*   安装 Android Studio
*   安装 Java Development Kit (JDK)
*   安装 Android SDK
*   一台 Android 设备或模拟器

### 获取代码

克隆本仓库到本地：

```bash
git clone git@github.com:Gong-Mi/gm.git
# 或使用 HTTPS:
# git clone https://github.com/Gong-Mi/gm.git