<p align="center">
  <h1 align="center">🔌 damo_link</h1>
  <p align="center">32 位单片机烧录工具 · 基于 probe-rs 的 Windows 图形化烧录器</p>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/platform-Windows-0078D6?style=flat-square&logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/backend-probe--rs-ED8B00?style=flat-square" alt="probe-rs">
  <img src="https://img.shields.io/badge/gui-Slint-2379F4?style=flat-square" alt="Slint">
</p>

---

## 📸 界面预览

<p align="center">
  <img src="1.png" alt="damo_link 界面" width="80%">
</p>

## ✨ 功能特性

| | 功能 | 说明 |
|---|---|---|
| 🎨 | **三套主题** | 深色 / 米白色 / 白色，右上角齿轮一键切换 |
| 💾 | **配置自动保存** | 芯片、主题、协议等改动自动记住，下次打开自动恢复 |
| 🔍 | **探针自动枚举** | 自动发现 DAPLink / ST-Link / J-Link 等调试探针 |
| 🧩 | **芯片三级级联** | 厂商 → 系列 → 型号，逐级筛选 |
| ⚡ | **固件操作** | 烧录 / 校验 / 擦除 / 复位，烧录成功自动复位运行 |
| 📜 | **实时日志** | probe-rs 输出流式显示、自动滚底、按状态着色 |

## 🚀 快速开始

1. 下载本目录全部文件
2. 运行 `damo_link.exe`
3. 点「刷新探针」→ 选择芯片 → 选择固件 → 点「烧录 Flash」

## 📁 目录结构

```
damo_link/
├── damo_link.exe        # 主程序（GUI）
├── probe-rs/
│   └── probe-rs.exe     # 烧录后端（子进程调用）
├── README.md
└── .gitignore
```

## ⚙️ 说明

- 烧录后端 `probe-rs\probe-rs.exe` 需与主程序保持同一目录结构，否则可在「设置」中手动指定路径
- 首次运行后会在同目录生成 `damo_link_config.json` 保存你的设置（该文件不随仓库分发）
