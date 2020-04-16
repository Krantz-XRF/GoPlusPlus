# GoPlusPlus

[![Build Status](https://travis-ci.org/Krantz-XRF/GoPlusPlus.svg?branch=master)](https://travis-ci.org/Krantz-XRF/GoPlusPlus)

围棋，用于记谱或实验。

## 软件依赖

这个程序依赖于`wxWidgets`，编写时的环境为3.1.0，要正确编译，您可能需要`wxWidgets 3.0`以上的版本。

## 软件语言

中文，当前没有添加其他语言支持的计划。

## 下载并使用

下载适用于Windows的[Github发布包](https://github.com/Krantz-XRF/GoPlusPlus/releases/tag/v1.0)。

## 编译指南

已迁移到CMake。现在您不需要修改生成脚本即可在所有支持CMake的平台编译。

### 使用 CMake 从源代码编译

按正常的CMake编译流程即可。例如：

```bash
mkdir build && cd build
cmake ..
cmake --build .
```

### 有关资源文件

为Windows平台下的方便，涉及的所有图片都以资源的形式插入可执行文件中。

在不支持资源的非Windows平台，您应当把对应的图片放在编译出的可执行文件路径下。

## 运行截图

| 图1 新棋局的编辑                 | 图2 打开已保存的棋局并继续编辑                 |
| -------------------------------- | ---------------------------------------------- |
| ![New-Game](screenshots/new.jpg) | ![Reopen-Game](screenshots/reopen.jpg)         |
| 图中为中国流布局的一种变化。     | 这种情况下，您将不能撤销到未标序号的那些棋步。 |
