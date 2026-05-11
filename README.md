# 🤖 xuebadiClaw🦞 

> 基于 X-OmniClaw 开源项目构建的中文定制版 AI 伴侣应用

[![Release](https://img.shields.io/github/v/release/xuebadi/xuebadiClaw)](https://github.com/xuebadi/xuebadiClaw/releases/latest)
[![APK Size](https://img.shields.io/github/release-assets-prepro/xuebadi/xuebadiClaw?label=APK%20Size)](https://github.com/xuebadi/xuebadiClaw/releases/latest)
[![License](https://img.shields.io/github/license/xuebadi/xuebadiClaw)](LICENSE)

## 🦞 简介

xuebadiClaw 是基于 [X-OmniClaw](https://github.com/OPPO-Mente-Lab/X-OmniClaw) 开源项目构建的中文定制版 AI 伴侣应用。

使用 Claude 等大语言模型作为思考引擎，通过 Android 无障碍服务实现自动化操作，让手机能够自主完成 App 搜索、购物比价、相册管理、视频创作等任务。

## ✨ 功能特性

- **中文优先**: 默认中文界面，贴近国内用户使用习惯
- **10+ 内置技能**: App 搜索、淘宝搜索、相册问答、剪映主题视频、自动化任务等
- **多模型支持**: 支持 OpenRouter / Anthropic / OpenAI / Moonshot / MiniMax / Ollama 等多种 AI 模型
- **跨平台扩展**: 支持飞书、Discord 等消息平台接入
- **自控模块**: 内置服务控制、ADB 调试、导航等自控技能

## 🧠 内置技能

| 技能 | 功能描述 |
|------|---------|
| app-search | 智能搜索手机中的应用 |
| taobao-search | 淘宝商品搜索与比价 |
| gallery-qa | 相册内容智能问答 |
| capcut-theme-video | 剪映主题视频自动创作 |
| scheduled-automation | 定时任务自动化 |
| navigation-skill | 导航与路径规划 |
| service-control | Android 服务控制 |
| adb-skill | ADB 调试技能 |
| config-skill | 配置管理与查看 |

## 🚀 安装

### 环境要求

- Android 9.0+ (API 28+)
- 无障碍服务权限
- 悬浮窗权限（可选）
- 存储/相册权限（可选）

### 安装步骤

1. **下载 APK**: 从 [Releases](https://github.com/xuebadi/xuebadiClaw/releases) 下载最新版本
2. **安装应用**: 在手机上打开 APK 文件安装
3. **开启权限**: 首次打开后，按照引导开启以下权限：
   - 无障碍服务 (必须)
   - 悬浮窗 (推荐)
   - 存储/相册 (可选)
4. **配置模型**: 填写 AI 模型的 API Key

### API Key 配置

支持的模型提供商：

| 提供商 | 配置方式 | 说明 |
|--------|--------|------|
| OpenRouter | `openrouter://anthropic/claude-3-5-sonnet` | 推荐，支持 Claude/Google 等 |
| Anthropic | `anthropic:sk-xxx` | Claude API |
| OpenAI | `openai:gpt-xxx` | GPT-4o |
| Moonshot | `moonshot:sk-xxx` | Moonshot AI (国内) |
| MiniMax | `minimax:sk-xxx` | Minimax (国内) |
| Ollama | `ollama:localhost:11434` | 本地模型 |

## 📖 使用

### 首次配置

1. 打开应用，进入模型配置页面
2. 选择模型提供商，填写 API Key
3. 选择模型版本（如 `claude-3-5-sonnet-20241022`）
4. 保存配置

### 基础操作

- **发起任务**: 在对话框中描述你想完成的任务
- **查看状态**: 顶部状态栏显示当前 Agent/任务状态
- **技能市场**: 管理已安装的技能

### 权限说明

| 权限 | 用途 | 必须 |
|------|------|------|
| 无障碍 | 读取屏幕、控制界面 | ✅ 是 |
| 悬浮窗 | 显示悬浮球、状态 | ❌ 否 |
| 存储 | 保存截图、相册分析 | ❌ 否 |
| 录屏 | 屏幕录制 | ❌ 否 |
| 相机 | 摄像头交互 | ❌ 否 |
| 麦克风 | 语音输入 | ❌ 否 |

## 🛠️ 开发

### 从源码构建

```bash
# 克隆仓库
git clone https://github.com/xuebadi/xuebadiClaw.git
cd xuebadiClaw

# 配置 Android SDK
echo "sdk.dir=/path/to/android-sdk" > local.properties

# 构建 Debug APK
./gradlew :app:assembleDebug

# 输出路径: app/build/outputs/apk/debug/xuebadiClaw-v{version}-debug.apk
```

### 技术栈

- **语言**: Kotlin + Python
- **框架**: Android Jetpack
- **AI**: Claude/GPT/Ollama
- **构建**: Gradle 7.5

## 📄 开源许可

本项目基于 X-OmniClaw 开源项目的修改版本，遵循相同的开源协议。

详见 [LICENSE](LICENSE) 文件。

## 🙏 致谢

- [X-OmniClaw](https://github.com/OPPO-Mente-Lab/X-OmniClaw) - 原始开源项目
- [Anthropic](https://www.anthropic.com) - Claude AI
- [OPPO Mente Lab](https://github.com/OPPO-Mente-Lab) - 项目发起团队

## 📦 相关链接

- [Releases](https://github.com/xuebadi/xuebadiClaw/releases)
- [Issue Tracker](https://github.com/xuebadi/xuebadiClaw/issues)
- [X-OmniClaw 原始仓库](https://github.com/OPPO-Mente-Lab/X-OmniClaw)
