# Obsidian AI Tagger Universe 🌌

[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](https://opensource.org/licenses/GPL-3.0)
[![Obsidian Downloads](https://img.shields.io/badge/Obsidian-Plugin-purple.svg)](https://obsidian.md/)

An intelligent tag management system for Obsidian, powered by Large Language Models (LLMs). Automatically clean, merge, and organize your vault's tags with semantic understanding.

---

## 🌟 Key Features / 核心功能

### 1. Smart Tag Deduplication (AI Merge) / AI 智能标签合并
- **Semantic Analysis**: Unlike simple string matching, it understands that `#DeepLearning` and `#deep-learning` (or even `#深度学习`) might be meant as the same tag.
- **Folder Scoping**: Run the analysis on a specific folder to handle domain-specific tags safely.
- **Interactive Review**: Review AI suggestions in a clear, modern GUI before applying changes.
- **Global Replacement**: Once confirmed, the plugin automatically renames tags across your entire vault while deduplicating existing ones.

### 2. Multi-Model Support / 多模型供应商支持
- Broad compatibility with major LLM providers: **OpenAI, Claude (Anthropic), DeepSeek, Aliyun (Qwen), Groq, OpenRouter, AWS Bedrock, Mistral, Cohere, and more.**
- Optimized API endpoint handling—no more manual URL hacking for non-OpenAI providers.
- Custom temperature controls for merge sensitivity.

### 3. Context-Aware Tagging / 上下文感知标签
- Uses **filename and adjacent tag context** during analysis to ensure merging logic respects the specific topics of your notes.
- Hardened parsing logic to handle complex vault structures without performance bottlenecks.

---

## 🚀 Installation / 安装

### Manual Installation
1. Download the `main.js`, `manifest.json`, and `styles.css` from the [Latest Release](https://github.com/your-repo/releases).
2. Create a folder named `ai-tagger-universe` in your vault's `.obsidian/plugins/` directory.
3. Move the downloaded files into that folder.
4. Go to **Obsidian Settings > Community Plugins** and enable "AI Tagger Universe".

---

## 📖 Usage / 使用说明

### 🧹 Deduplicating Tags (Merge Similar)
1. **Right-click** on any folder in your file explorer.
2. Select **"AI Merge Similar Tags in this Folder"**.
3. Confirm the action in the prompt.
4. Review the AI-generated merge groups:
   - **Keep**: The suggested target tag.
   - **Merge**: List of tags that will be absorbed.
5. Click **"Merge This"** for specific groups, or **"Merge All"** to batch process.

### ⚙️ Configuration
- **API Key**: Enter your provider's API key in the plugin settings.
- **Provider Settings**: Select your service (OpenAI, Local, or Custom Cloud).
- **Merge Sensitivity**: Adjust the temperature in settings to make the AI more or least aggressive with merges.

---

## 🛠️ Development / 开发

This plugin is built with TypeScript and utilizes the Obsidian API.

```bash
# Install dependencies
npm install

# Build for production
npm run build
```

---

## 📄 License / 许可证

GPL-3.0 License. See [LICENSE](LICENSE) for details.

---

## 🤝 Support / 支持

If you find this plugin helpful, consider giving it a ⭐ on GitHub! 
如果你觉得这个插件有帮助，请在 GitHub 上点个 ⭐！
