name: PlatformIO-skill
description: 通过Python实现PlatformIO项目的构建、上传、监控

# PlatformIO 技能

此技能提供通过Python脚本自动化PlatformIO项目工作流程的指导，包括构建、上传、监控、依赖管理等功能。

## 使用场景

- 自动化CI/CD流水线中的固件构建
- 批量处理多个PlatformIO项目
- 集成PlatformIO到Python自动化脚本中
- 监控串口输出并自动处理日志
- 动态修改platformio.ini配置

## 方法：直接使用python -m platformio命令

PlatformIO是一个Python模块，可以直接通过`python -m platformio`调用。这是最直接的Python调用方式，与命令行使用完全一致。

### 基本语法

```bash
# 在终端中直接使用
python -m platformio [命令] [选项]

# 在Python脚本中使用
import subprocess
subprocess.run(["python", "-m", "platformio", "命令", "选项"])
```

### 常用命令示例

```bash
# 1. 构建项目
python -m platformio run

# 2. 清理构建文件
python -m platformio run -t clean

# 3. 上传固件
python -m platformio run -t upload

# 4. 监控串口输出
python -m platformio device monitor

# 5. 指定串口和波特率
python -m platformio device monitor --port COM3 --baud 115200

# 6. 构建特定环境
python -m platformio run -e esp32-s3-devkitm-1

# 7. 安装库
python -m platformio lib install "库名"

# 8. 列出设备
python -m platformio device list
```
