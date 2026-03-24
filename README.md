<!-- doubao-image-generator/README.md -->

<div align="center">

# 🎨 doubao-image-generator

豆包 AI 图片生成自动化工作流

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-Skill-orange.svg)](https://github.com/openclaw)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)]()

*通过浏览器自动化在豆包 (www.doubao.com) 生成图片*

</div>

---

## 📖 项目简介

doubao-image-generator 是一个基于 OpenClaw 的 AI 图片生成自动化技能。它通过浏览器自动化技术，帮助用户快速在豆包 AI 平台上生成各类图片素材，包括海报、插画、贴纸、头像等。

本技能完全自动化执行：自动打开豆包 → 进入图片生成模式 → 输入描述 Prompt → 等待生成 → 下载图片，全程无需手动操作。

为没有文生图API的平替方案,或者token cooldown的暂替方案。

---

## ✨ 功能特点

| 功能 | 描述 |
|------|------|
| 🎬 海报设计 | 社交媒体海报、活动宣传图、产品海报 |
| 🎨 插画创作 | 博客配图、文章封面、故事插画 |
| 📌 贴纸设计 | 表情贴纸、IP 形象贴纸、主题贴纸 |
| 👤 头像生成 | 个人头像、卡通形象、商务头像 |

### 核心特性

- 🤖 **全自动执行** - 无需手动操作，AI 帮你完成整个流程
- 🎯 **智能识别** - 自动识别生成、画图、创建等关键词触发执行
- 💬 **中文优化** - 对中文 Prompt 有更好的理解能力
- 🔄 **多图选择** - 支持生成多张图片供选择
- 📥 **自动下载** - 选中图片后自动下载保存

---

## 🛠️ 技术栈

| 技术 | 说明 |
|------|------|
| [OpenClaw](https://github.com/openclaw) | AI 助手框架 |
| [Browser MCP](https://github.com/openclaw/browser) | 浏览器自动化控制 |
| [豆包 AI](https://www.doubao.com) | AI 图片生成服务 |

---

## 📋 前置要求

在开始使用本技能前，请确保满足以下条件：

### 1. 环境要求

- **操作系统**：macOS / Linux / Windows
- **浏览器**：Google Chrome 已安装
- **Node.js**：v18.0.0 或更高版本

### 2. 账号要求

- ✅ 已注册豆包账号（如未注册，请访问 [www.doubao.com](https://www.doubao.com) 注册）

### 3. OpenClaw 配置

确保 OpenClaw 已正确安装并配置好浏览器：

```bash
# 检查 OpenClaw 状态
openclaw gateway status

# 如需启动
openclaw gateway start
```

---

## 🚀 安装方法

### 方法一：通过 ClawHub 安装（推荐）

```bash
# 安装最新版本的技能
clawhub install doubao-image-generator
```

### 方法二：手动安装

```bash
# 1. 克隆或下载本技能到本地
git clone https://github.com/openclaw/doubao-image-generator.git ~/.openclaw/skills/doubao-image-generator

# 2. 安装依赖（如有）
cd ~/.openclaw/skills/doubao-image-generator
npm install

# 3. 重启 OpenClaw 使技能生效
openclaw gateway restart
```

---

## 📖 使用方法

### 触发方式

当你对 AI 助手说出以下指令时，技能会自动执行：

| 指令示例 | 说明 |
|----------|------|
| "生成一张XX海报" | 生成指定主题的海报 |
| "帮我画一个XX头像" | 生成指定风格的头像 |
| "做一张XX贴纸" | 生成指定主题的贴纸 |
| "用豆包生成XX插画" | 生成指定内容的插画 |
| "创建一个XX图片" | 创建任意类型的图片 |

### 执行流程

```
用户输入需求
    ↓
AI 自动打开豆包 (www.doubao.com)
    ↓
检查登录状态（如未登录，提示扫码）
    ↓
进入图片生成模式
    ↓
输入用户描述的 Prompt
    ↓
等待图片生成（通常几秒到十几秒）
    ↓
展示生成结果，用户选择满意的图片
    ↓
下载保存到本地
    ↓
询问用户是否需要调整
```

### 交互示例

```
👤 用户：帮我生成一个可爱的小猫头像

🤖 AI：好的！帮你打开豆包生成一个可爱的小猫头像～
[自动执行中...]

🤖 AI：生成完成！请选择你喜欢的图片：
[展示生成的图片]

👤 用户：第一个不错

🤖 AI：[下载保存] 已保存到本地～ 
请问需要调整吗？比如换个颜色或者风格？
```

---

## 📝 示例 Prompt

以下是一些常用的 Prompt 示例，供你参考：

### 🎬 海报

```
人工智能主题海报，科技未来风格，神经网络网格背景，
机器人与人类握手，蓝色紫色赛博朋克配色，
现代设计感，视觉冲击力强，适合社交媒体传播，高清
```

### 👤 头像

```
AI女生助手卡通头像，美术编辑身份，简约而精致，
浅棕色长发微卷，头上戴着金色麦穗发箍，温柔甜美的微笑，
元气满满的眼神，艺术家风格，浅色系舒适上衣，
暖光洒入，清新干净，动漫风格，精致细节
```

### 📌 贴纸

```
禁毒主题贴纸，潮流街头风格，酷女孩手持禁止标志，
大字"禁毒"英文"SAY NO TO DRUGS"，简洁有力的线条，
扁平化设计，矢量风格，贴纸工艺效果，白色底
```

### 🎨 插画

```
森林主题插画，日系动漫风格，可爱的小狐狸在花丛中，
毛茸茸的大尾巴，梦幻森林背景，柔和配色，
精致细节，阳光透过树叶洒落，动漫CG风格
```

---

## 💡 Prompt 编写技巧

### 推荐结构

```
[主体描述] + [风格] + [配色] + [细节] + [技术参数]
```

### 常用风格关键词

| 风格类型 | 推荐关键词 |
|----------|------------|
| 卡通/动漫 | 卡通风格、动漫风格、二次元、Q版 |
| 潮流 | 潮流风格、街头风、酷炫、扁平化 |
| 可爱 | 可爱风格、萌趣、卡通形象 |
| 写实 | 写实风格、精细细节、高清 |
| 国风 | 中国风、国潮、水墨、传统元素 |
| 极简 | 极简风格、简约、现代设计 |

### 增效关键词

在 Prompt 末尾添加以下词汇可提升效果：

```
高清画质，精细细节
数字艺术作品
柔和的光影
干净的背景
```

---

## ⚠️ 注意事项

### 1. 中文 Prompt 效果更佳 🇨🇳

豆包对中文理解更加准确，建议使用中文描述图片内容。英文关键词可以作为补充，但主体描述推荐用中文。

### 2. 分步描述更清晰

对于复杂画面，建议先描述主体，再补充细节：
```
❌ 好看的小猫
✅ 可爱的橘猫，圆脸大眼，肉乎乎的脸颊，萌萌的表情
```

### 3. 明确风格关键词

风格描述要具体，避免使用模糊词汇：
```
❌ 好看一点
✅ 二次元漫画风格、赛博朋克风格
```

### 4. 耐心等待生成

图片生成通常需要几秒到十几秒，请耐心等待。如果长时间无响应，可检查网络连接或豆包服务器状态。

### 5. 登录状态

首次使用需要登录豆包账号。如提示登录，请扫码完成登录后继续使用。

---

## ❓ 常见问题

### Q1: 提示需要登录怎么办？

**A**: 豆包账号未登录时，会提示你扫码登录。完成登录后告诉 AI 即可继续执行。

### Q2: 生成速度慢怎么办？

**A**: 
- 检查网络连接是否稳定
- 豆包服务器繁忙时可能需要等待更长时间
- 可使用 `browser(action: snapshot)` 查看生成进度

### Q3: 生成结果不满意怎么办？

**A**: 
- 收集具体反馈（如颜色、风格、细节等）
- 重新生成时调整 Prompt 描述
- 豆包支持一次生成多张图片，可选择最满意的

### Q4: 支持哪些图片格式？

**A**: 豆包支持 PNG、JPG 等常见格式，下载时通常为 PNG 格式。

### Q5: 可以生成中文文字吗？

**A**: 可以，但在 Prompt 中需要明确写出文字内容（如"大字'禁毒'"），生成效果会更准确。

---

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

### 提交 Issue

请包含以下信息：
- 操作系统环境
- 复现步骤
- 预期 vs 实际结果
- 截图（如有）

### 提交 PR

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/xxx`)
3. 提交更改 (`git commit -m 'Add xxx'`)
4. 推送分支 (`git push origin feature/xxx`)
5. 创建 Pull Request

---

## 📄 License

本项目基于 MIT License 开源 - 详见 [LICENSE](./LICENSE) 文件。

---

## 📧 联系作者

如果你有任何问题或建议，欢迎通过以下方式联系：

- **GitHub Issues**: [https://github.com/openclaw/doubao-image-generator/issues](https://github.com/openclaw/doubao-image-generator/issues)
- **OpenClaw 社区**: [https://github.com/openclaw/openclaw](https://github.com/openclaw/openclaw)

---

<div align="center">

*如果这个技能对你有帮助，欢迎 ⭐ Star 支持！*

</div>
