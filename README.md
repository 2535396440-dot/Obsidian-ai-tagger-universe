# Obsidian AI Tagger Universe

借助 AI 对该插件进行改进 / Improved version of the plugin utilizing AI.

## English
This plugin allows you to automatically tag your markdown files using LLMs.

### New Features (Updated)

1. **AI Merge Similar Tags in Current Folder** 
   - A new command "AI Merge Similar Tags in Current Folder" is available!
   - When triggered, it will correctly identify the current folder you are operating in.
   - It will show a confirmation modal with a 45-second countdown to ensure you want to send folder data.
   - Once confirmed, it efficiently extracts tags via the native Obsidian `metadataCache` logic without heavy traversals.
   - It logically bypasses the plugin's original hardcoded SYSTEM_PROMPT to supply an intelligent structure-driven analysis prompt, preventing prompt conflicts while maintaining core features.
   - It delegates the merge strategy to the AI model using a predefined JSON prompt template, now enhanced with **filename contextual awareness** to better understand the domain.
   - Intelligent data structure validations prevent unexpected outputs from disrupting plugin operations.
   - Displays real-time progress via non-obtrusive `Notice` pop-ups.
   - Allows users to review the AI suggestions in a clean list GUI and selectively apply updates globally across the vault.
   - Command is fully bindable to custom hotkeys in Obsidian Settings.

2. **Multiple LLM Provider Support (Patched Endpoints)**
   - Fixed endpoint handling for various providers like Aliyun, Claude, Deepseek, Groq, OpenRouter, AWS Bedrock, Mistral, Requesty, Cohere, and Grok.
   - No longer restricted to OpenAI compatible URLs, making configuration much simpler!

## 中文 (Chinese)
此插件可通过各家大语言模型 (LLM) 智能分析并为你的笔记自动生成、补全、或合并不一致的标签。

### 新功能 (最近更新)

1. **在当前文件夹内 AI 合并相似标签**
   - 新增了 "AI 智能合并当前文件夹标签" (AI Merge Similar Tags in Current Folder) 命令。
   - 当执行时，会弹窗请求操作所在的目录，附带撤销执行按钮和 45 秒倒计时自动关闭的安全机制。
   - 用户确认后，通过原生的 `metadataCache` 提取标签，无需重型遍历，极大提高了检测效率。
   - 巧妙绕过了原插件硬编码 System Prompt 导致的指令冲突，为合并任务下发了高强度的结构化判定词，互不影响核心功能。
   - 采用 JSON 模板对提取的标签及其所在的**文件名上下文**进行组装，发送给大模型进行更精准的领域和语义合并分析。
   - 增加了底层数据结构“硬拦截”校验，避免大模型输出杂乱内容导致应用崩溃。
   - 全链路（分析标签、请求 AI、AI 接收与思考）提供友好轻量且不打扰的角标 `Notice` 提醒。
   - AI 分析后，复用了非常友好的重命名视图界面，允许用户进行差异比对、合并并保留自己需要的原标签。
   - 虽然合并建议基于当前文件夹，但**最终合并重命名操作将全局应用于整个 Obsidian 库**。
   - 原生支持 Obsidian 快捷键绑定设置。

2. **完善的第三方 LLM 端点兼容**
   - 彻底重写了包括 Deepseek、阿里云 (Qwen)、Claude、Groq、OpenRouter、AWS Bedrock 等 10+ 家 AI 供应商端点的 API Endpoint 生成逻辑。
   - 避免了先前只能顺滑使用 OpenAI 或必须自行手拼复杂 Endpoint 的困境。
