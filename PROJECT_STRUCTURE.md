# 校园网自动登录工具 - 项目结构

## 📁 目录结构（精简版）

```
campus/                       # 项目根目录
├── auto_campus_login.py      # CLI版本主程序
├── campus_login_gui.py       # GUI版本主程序
├── requirements.txt          # Python依赖
├── login_config.json.example # 配置示例
├── README.md                 # 项目主文档
├── PROJECT_STRUCTURE.md      # 项目结构说明（当前文件）
├── LICENSE                   # MIT许可证
├── icon.ico                  # 程序图标
├── 运行GUI.bat              # Windows启动脚本
├── build_config_optimized.spec # PyInstaller打包配置
├── .mcp.json                # GitHub MCP配置
└── .gitignore               # Git忽略配置

build/                        # PyInstaller构建目录（已忽略）
dist/                         # 打包输出目录（已忽略）
```

## 🎯 核心文件说明

### 主程序文件
- **auto_campus_login.py** (474行) - CLI版本，支持命令行参数和监控模式
- **campus_login_gui.py** (1360行) - GUI版本，支持系统托盘和主题切换

### 配置文件
- **requirements.txt** - Python第三方库依赖列表
- **login_config.json.example** - 用户配置示例（实际配置文件被忽略）
- **build_config_optimized.spec** - PyInstaller打包优化配置

### 文档和资源
- **README.md** - 项目使用说明和功能介绍
- **PROJECT_STRUCTURE.md** - 项目结构文档（当前文件）
- **LICENSE** - MIT开源许可证
- **icon.ico** - 程序图标文件
- **运行GUI.bat** - Windows系统快速启动脚本

### 开发工具
- **.mcp.json** - GitHub MCP服务器配置（用于发布管理）
- **.gitignore** - Git版本控制忽略规则

## 🔧 技术特性

### 网络探测优化（V2.7核心功能）
- 抖音、OPPO、百度三站点冗余探测
- 3次失败确认机制，零误判"假断网"
- 10秒内完成重连确认（4倍速度提升）
- 5秒快速重试机制

### 核心功能
- 自动检测校园网认证入口
- 支持多种密码加密方式
- 系统托盘后台运行
- 深色/浅色主题切换
- Windows开机自启
- 完整的日志系统

## 🚀 快速开始

### 源码运行
```bash
pip install -r requirements.txt
python campus_login_gui.py    # 运行GUI版本
python auto_campus_login.py -u username -p password  # 运行CLI版本
```

### 打包可执行文件
```bash
pyinstaller build_config_optimized.spec --clean
```

## 📋 文件大小
- 源代码：约 71KB（3个Python文件）
- 打包后：约 18MB（单文件可执行程序）

## 📝 版本信息
- 当前版本：V2.7
- 主要改进：网络探测算法优化
- 发布日期：2025-11-23

---
**最后更新：2025-11-23**