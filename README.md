# Qwen Code - 智能编程助手

Qwen Code 是一个专为开发者设计的 AI 编程助手工具，提供智能代码补全、优化建议和错误检测功能。

## 🚀 安装指南

### 系统要求
- Node.js >= 20.0.0
- 支持 macOS、Linux、Windows

### 标准安装流程
```bash
# 1. 克隆项目
git clone https://github.com/carlos-wong/qwen-code.git
cd qwen-code

# 2. 安装依赖
npm install

# 3. 构建项目
npm run build

# 4. 全局安装
npm install -g .
```

## 🔧 启动配置

### 环境变量设置

在使用 Qwen Code 之前，需要配置以下环境变量：

#### GLM 模型配置
```bash
# 设置 GLM API 基础 URL
export GLM_OPENAI_BASE_URL="https://open.bigmodel.cn/api/paas/v4"

# 设置 GLM 模型名称
export GLM_OPENAI_MODEL="glm-4-flash"

# 设置 GLM API 密钥
export GLM_OPENAI_API_KEY="your-glm-api-key-here"
```

#### 永久保存环境变量
**macOS/Linux (bash/zsh):**
```bash
# 编辑 ~/.bashrc 或 ~/.zshrc
echo 'export GLM_OPENAI_BASE_URL="https://open.bigmodel.cn/api/paas/v4"' >> ~/.bashrc
echo 'export GLM_OPENAI_MODEL="glm-4-flash"' >> ~/.bashrc
echo 'export GLM_OPENAI_API_KEY="your-glm-api-key-here"' >> ~/.bashrc

# 重新加载配置
source ~/.bashrc
```

**macOS (fish shell):**
```bash
# 编辑 ~/.config/fish/config.fish
echo 'set -x GLM_OPENAI_BASE_URL "https://open.bigmodel.cn/api/paas/v4"' >> ~/.config/fish/config.fish
echo 'set -x GLM_OPENAI_MODEL "glm-4-flash"' >> ~/.config/fish/config.fish
echo 'set -x GLM_OPENAI_API_KEY "your-glm-api-key-here"' >> ~/.config/fish/config.fish
```

### 启动方式

#### 基本启动
```bash
qwen
```

#### 使用 GLM 环境变量启动
```bash
OPENAI_BASE_URL=$GLM_OPENAI_BASE_URL OPENAI_MODEL=$GLM_OPENAI_MODEL OPENAI_API_KEY=$GLM_OPENAI_API_KEY qwen
```

#### 调试模式启动
```bash
npm run debug
```

## ⚠️ 兼容性说明

### 已移除的不兼容模式
- **移除了 OpenAI 原生模式**：不再直接支持 OpenAI API，专注于 GLM 模型优化
- **移除了多模型并行模式**：简化为单一 GLM 模型支持，确保稳定性
- **移除了实验性功能**：去除了可能影响智谱兼容性的实验性特性

### GLM 优化特性
- ✅ 完全兼容 GLM-4-Flash 模型
- ✅ 针对 GLM API 进行了专门优化
- ✅ 支持 GLM 的流式响应
- ✅ 适配 GLM 的错误处理机制

## 📦 开发命令

```bash
# 完整项目检查
npm run preflight

# 运行测试
npm run test

# 代码规范检查
npm run lint

# 构建项目
npm run build

# 打包项目
npm run bundle

# 格式化代码
npm run format
```

## 🌟 主要功能

- **智能代码补全**：基于 GLM 模型的上下文感知代码建议
- **代码优化**：自动识别性能瓶颈并提供优化方案
- **错误检测**：实时发现代码中的潜在问题
- **多语言支持**：支持 JavaScript、TypeScript、Python 等主流语言
- **项目集成**：无缝集成到现有开发工作流中

## 📝 使用示例

```bash
# 启动交互式编程助手
qwen

# 在项目中使用
cd your-project
qwen --help
```

## 🌐 仓库地址

[https://github.com/carlos-wong/qwen-code](https://github.com/carlos-wong/qwen-code)

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request 来改进项目！