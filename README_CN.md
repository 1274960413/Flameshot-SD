<div align="center">
  <p>
    <h1>
      <a href="https://github.com/flameshot-org/flameshot">
        <img src="data/img/app/org.flameshot.Flameshot.svg" alt="Flameshot" width="128" />
      </a>
      <br />
      Flameshot
    </h1>
    <h4>功能强大且简单易用的截图软件</h4>
  </p>
  <p>
    <a href="https://github.com/flameshot-org/flameshot/releases">
      <img src="https://img.shields.io/github/release/flameshot-org/flameshot.svg" alt="最新版本" />
    </a>
    <a href="https://github.com/flameshot-org/flameshot/blob/master/LICENSE">
      <img src="https://img.shields.io/github/license/flameshot-org/flameshot.svg" alt="许可证" />
    </a>
  </p>
</div>

---

## 目录

- [项目简介](#项目简介)
- [功能特性](#功能特性)
- [截图预览](#截图预览)
- [使用方法](#使用方法)
  - [图形界面](#图形界面)
  - [命令行](#命令行)
  - [全局快捷键](#全局快捷键)
- [快捷键说明](#快捷键说明)
- [编译安装](#编译安装)
  - [Windows](#windows)
  - [依赖说明](#依赖说明)
- [最新功能](#最新功能)
- [许可证](#许可证)

---

## 项目简介

**Flameshot** 是一款开源的跨平台截图工具，支持 Linux、Windows 和 macOS 系统。它提供了丰富的截图编辑功能，包括标注、箭头、文字、模糊等工具，让您可以轻松地对截图进行编辑和分享。

本项目是基于官方 Flameshot 的增强版本，新增了**剪贴板贴图**功能，类似于 Snipaste 的贴图功能。

---

## 功能特性

### 核心截图功能
- **区域截图** - 自由选择截图区域
- **全屏截图** - 截取整个屏幕
- **窗口截图** - 截取指定窗口
- **延迟截图** - 支持设置延迟时间（用于截取鼠标悬停提示等）

### 截图编辑工具
| 工具 | 说明 | 快捷键 |
|------|------|--------|
| 铅笔 | 自由手绘 | P |
| 直线 | 绘制直线 | D |
| 箭头 | 绘制箭头 | A |
| 矩形 | 绘制矩形框 | R |
| 圆形 | 绘制圆形 | C |
| 文字 | 添加文字 | T |
| 标记 | 高亮标记 | M |
| 马赛克 | 模糊/像素化处理 | B |
| 反色 | 颜色反转 | I |
| 序号 | 添加序号标记 | 无 |

### 截图后操作
- **保存** - 保存到文件 (Ctrl+S)
- **复制** - 复制到剪贴板 (Ctrl+C)
- **固定** - 将截图固定到屏幕上
- **上传** - 上传到 Imgur（可选）
- **打开** - 用其他程序打开

### 贴图功能（新增）
- **剪贴板贴图** - 将剪贴板中的图片或文字固定到屏幕
- **文字渲染** - 支持多行文字显示
- **贴图操作** - 支持拖动、缩放、旋转、调整透明度
- **全局快捷键** - 支持自定义快捷键触发贴图

---

## 截图预览

![使用演示](https://raw.githubusercontent.com/flameshot-org/flameshot/master/data/img/preview/animatedUsage.gif)

---

## 使用方法

### 图形界面

启动 Flameshot 后，系统托盘会出现火焰图标：

1. **左键点击** - 开始区域截图
2. **右键点击** - 打开菜单（配置、关于、退出等）

### 命令行

```bash
# 区域截图（GUI 模式）
flameshot gui

# 全屏截图
flameshot full

# 截图并保存到指定路径
flameshot gui -p ~/Pictures/Screenshots

# 延迟 2 秒后截图
flameshot gui -d 2000

# 截图并固定到屏幕
flameshot gui --pin

# 贴图模式（将剪贴板内容固定到屏幕）- 新增功能
flameshot pin
```

### 全局快捷键

#### Windows
| 功能 | 默认快捷键 |
|------|-----------|
| 截图 | Win+Shift+X |
| 贴图 | Ctrl+Shift+V |

#### macOS
| 功能 | 默认快捷键 |
|------|-----------|
| 截图 | Ctrl+Shift+X |
| 贴图 | Ctrl+Shift+V |

#### 自定义快捷键
1. 右键点击系统托盘图标
2. 选择"配置"
3. 进入"快捷键"选项卡
4. 设置你喜欢的快捷键

---

## 快捷键说明

### 截图模式快捷键

| 快捷键 | 功能 |
|--------|------|
| P | 铅笔工具 |
| D | 直线工具 |
| A | 箭头工具 |
| S | 选择工具 |
| R | 矩形工具 |
| C | 圆形工具 |
| M | 标记工具 |
| T | 文字工具 |
| B | 马赛克工具 |
| I | 反色工具 |
| Ctrl+C | 复制到剪贴板 |
| Ctrl+S | 保存到文件 |
| Ctrl+Z | 撤销 |
| Ctrl+Shift+Z | 重做 |
| Esc | 退出截图 |
| 空格 | 显示/隐藏侧边栏 |
| 鼠标滚轮 | 调整工具大小 |

### 贴图模式快捷键

| 快捷键 | 功能 |
|--------|------|
| 1-0 | 调整透明度（10%-100%）|
| Ctrl+Q | 关闭贴图 |
| Esc | 关闭贴图 |
| 鼠标滚轮 | 缩放贴图 |
| 双击 | 关闭贴图 |

---

## 编译安装

### Windows

#### 环境要求
- Visual Studio 2022
- CMake >= 3.22
- Qt6 >= 6.2.4

#### 编译步骤

```powershell
# 1. 克隆仓库
git clone https://github.com/flameshot-org/flameshot.git
cd flameshot

# 2. 创建构建目录
mkdir build
cd build

# 3. 配置 CMake
cmake .. -G "Visual Studio 17 2022" -A x64 `
  -DCMAKE_BUILD_TYPE=Release `
  -DCMAKE_PREFIX_PATH="C:\Qt\6.x.x\msvc2022_64" `
  -DENABLE_OPENSSL=OFF

# 4. 编译
cmake --build . --config Release --parallel

# 5. 运行
.\src\Release\flameshot.exe
```

### 依赖说明

#### 必需依赖
- Qt6 Core、Gui、Widgets、Network、Svg
- CMake >= 3.22
- 编译器支持 C++20

#### 自动获取的依赖
- Qt-Color-Widgets - 颜色选择器
- KDSingleApplication - 单实例支持
- QHotkey - 全局快捷键支持

---

## 最新功能

### v14.0.0+ 新增功能

#### 1. 剪贴板贴图功能
- 支持将剪贴板中的图片固定到屏幕
- 支持将文字渲染为图片并固定
- 支持多行文字显示

#### 2. 全局快捷键支持
- 新增 `PIN_CLIPBOARD` 快捷键配置
- 支持自定义贴图快捷键
- 默认快捷键：Ctrl+Shift+V

#### 3. 贴图操作
- 鼠标拖动移动位置
- 滚轮缩放
- 数字键调整透明度
- 右键菜单：复制、保存、旋转

#### 4. 命令行支持
```bash
# 贴图命令
flameshot pin
```

---

## 项目结构

```
flameshot/
├── src/                    # 源代码
│   ├── cli/               # 命令行接口
│   ├── config/            # 配置管理
│   ├── core/              # 核心功能
│   ├── tools/             # 截图工具
│   │   └── pin/          # 贴图功能（新增）
│   ├── utils/             # 工具类
│   └── widgets/           # UI 组件
├── data/                   # 资源文件
├── docs/                   # 文档
└── packaging/              # 打包配置
```

---

## 许可证

本项目采用 GPLv3 许可证开源。

- 主代码：GPLv3
- Logo：Free Art License v1.3
- 按钮图标：Apache License 2.0

---

## 致谢

感谢以下项目和贡献者：
- [Qt-Color-Widgets](https://github.com/mbasaglia/Qt-Color-Widgets) - 颜色选择器组件
- [KDSingleApplication](https://github.com/KDAB/KDSingleApplication) - 单实例支持
- [QHotkey](https://github.com/Skycoder42/QHotkey) - 全局快捷键支持
- 所有贡献者和翻译者

---

<div align="center">
  <p>
    <a href="https://flameshot.org">官方网站</a> |
    <a href="https://github.com/flameshot-org/flameshot">GitHub</a> |
    <a href="https://flameshot.org/docs/">文档</a>
  </p>
</div>
