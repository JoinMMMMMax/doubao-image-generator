# 🎨 doubao-image-generator 安装指南

本指南将帮助你完成豆包 AI 图片生成技能的安装和配置。

---

## 📋 目录

- [环境要求](#-环境要求)
- [安装步骤](#-安装步骤)
- [配置说明](#-配置说明)
- [验证安装](#-验证安装)
- [常见问题](#-常见问题)

---

## 🖥️ 环境要求

### 1. Chrome 浏览器

- **必需**：Google Chrome 浏览器（最新版）
- macOS 用户：`brew install --cask google-chrome` 或从 [官网](https://www.google.com/chrome/) 下载
- Windows 用户：从 [官网](https://www.google.com/chrome/) 下载安装

### 2. OpenClaw 环境

- **必需**：OpenClaw 已正确安装并运行
- 确认方法：终端运行 `openclaw gateway status`，显示 `running` 即为正常

```bash
# 检查 OpenClaw 状态
openclaw gateway status

# 如需启动
openclaw gateway start
```

---

## 📥 安装步骤

### 方式一：使用 OpenClaw 自动安装（推荐）

如果你的 OpenClaw 已配置好，可以直接通过以下方式安装：

```bash
# 方式 1：使用 ClawHub 安装
clawhub install doubao-image-generator

# 方式 2：手动复制到 skills 目录
cp -r doubao-image-generator ~/.openclaw/skills/
```

### 方式二：手动安装

```bash
# 1. 进入 OpenClaw skills 目录
cd ~/.openclaw/skills

# 2. 克隆或复制技能文件夹
git clone <repo-url> doubao-image-generator

# 或手动创建目录并复制文件
mkdir -p doubao-image-generator
# 将 SKILL.md 等文件复制到该目录
```

---

## ⚙️ 配置说明

### 1. 浏览器配置

#### 启动 OpenClaw 浏览器服务

```bash
# 确保 OpenClaw gateway 已启动
openclaw gateway start

# 检查浏览器状态
openclaw browser status
```

#### 配置 Chrome 配置文件

技能使用 `profile: "openclaw"` 打开独立的浏览器配置：

- 如果是首次使用，OpenClaw 会自动创建新配置
- 如需使用已登录的豆包账号，可使用 `profile: "user"` 打开你的个人 Chrome

```javascript
// 技能会自动使用以下配置打开浏览器
browser(
  action: "open",
  url: "https://www.doubao.com",
  profile: "openclaw"
)
```

### 2. 豆包账号登录

#### 首次登录步骤

1. **触发技能**：告诉 AI 「帮我生成一张 xxx 图片」
2. **自动打开**：技能会自动打开豆包网站
3. **登录提示**：如未登录，页面会显示二维码
4. **扫码登录**：使用豆包 App 扫码完成登录
5. **继续执行**：登录成功后告诉 AI 「已登录」即可继续

#### 登录状态保持

- 首次登录后，浏览器会保存登录状态
- 后续使用通常无需再次登录
- 如遇登录失效，重复上述步骤即可

---

## ✅ 验证安装

### 快速测试

1. **启动 OpenClaw**（如未启动）：
   ```bash
   openclaw gateway start
   ```

2. **触发技能**：
   尝试对 AI 说：
   - "帮我生成一个可爱的小猫头像"
   - "做一张科技主题海报"

3. **检查流程**：
   - AI 应该自动打开 Chrome 浏览器
   - 导航到 www.doubao.com
   - 进入图片生成模式
   - 输入 Prompt 并生成图片

### 验证命令

```bash
# 检查技能是否被识别
openclaw skills list | grep doubao

# 检查浏览器是否可以正常打开
openclaw browser test
```

---

## ❓ 常见问题

### Q1: 打开浏览器失败怎么办？

**A**: 
1. 确认 Chrome 已正确安装：`open -a "Google Chrome"`
2. 检查 OpenClaw gateway 状态：`openclaw gateway status`
3. 尝试重启：`openclaw gateway restart`

### Q2: 提示需要登录怎么办？

**A**: 这是正常流程。请：
1. 使用豆包 App 扫描页面显示的二维码
2. 登录成功后告诉 AI 「已登录」
3. 技能会自动继续执行

### Q3: 生成速度很慢怎么办？

**A**: 
- 检查网络连接是否稳定
- 豆包服务器高峰期可能会慢一些
- 可以用 `browser(action: snapshot)` 查看生成进度

### Q4: 生成结果不满意怎么办？

**A**: 
- 收集具体反馈（颜色、风格、细节等）
- 告诉 AI 你的修改意见，如「颜色再亮一点」
- AI 会重新生成或调整 Prompt

### Q5: 图片无法下载怎么办？

**A**: 
- 检查浏览器弹窗拦截设置
- 尝试右键图片选择「另存为」
- 或截图保存

### Q6: 技能无法触发怎么办？

**A**: 
- 检查技能文件是否在正确位置：`~/.openclaw/skills/doubao-image-generator/`
- 确认 OpenClaw 已重新加载技能
- 可以尝试重启 OpenClaw gateway

---

## 📞 获取帮助

如果遇到其他问题：

1. 查看 [SKILL.md](./SKILL.md) 详细文档
2. 提交 GitHub Issue
3. 在 OpenClaw 社区寻求帮助

---

<div align="center">

*祝你使用愉快！🎨*

</div>
