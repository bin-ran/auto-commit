# Smart Commit Message

<div align="center">
  <a href="./README.zh.md">中文</a> | English
</div>

AI-powered VS Code extension that automatically analyzes Git code changes and generates high-quality commit messages.

## Features

- **AI Auto-Generation** — Analyzes `git diff` content and generates commit messages with one click
- **Source Control Integration** — Click the sparkle button directly in the Git panel
- **Multiple Styles** — Supports Conventional Commits, Simple, and Detailed modes
- **Bilingual Support** — Choose between Chinese or English for generated messages
- **Multi-Platform Compatible** — Supports OpenAI-format APIs (DeepSeek, OpenAI, etc.)
- **Custom Prompt** — Append custom system prompts to control generation behavior

## Installation

1. Search for "Smart Commit Message" in the VS Code Extension Marketplace
2. Click Install

## Usage

1. Edit your code in the editor
2. Open the **Source Control** panel (Ctrl+Shift+G)
3. Click the sparkle button in the toolbar, or press `Ctrl+Shift+P` and type **"Generate Commit Message"**
4. The generated commit message will be automatically filled into the input box

## Configuration

Search for `Smart Commit Message` in VS Code Settings:

| Setting | Description | Default |
| ------- | ----------- | ------- |
| `smartCommitMessage.apiKey` | API Key for the AI service | - |
| `smartCommitMessage.baseUrl` | OpenAI-compatible API base URL | `https://api.deepseek.com` |
| `smartCommitMessage.model` | Model name for commit generation | `deepseek-v4-flash` |
| `smartCommitMessage.style` | Commit message style (conventional / simple / detailed) | `conventional` |
| `smartCommitMessage.language` | Language for generated commits (English / Chinese) | `Chinese` |
| `smartCommitMessage.customPrompt` | Custom system prompt appended after the style template | - |

## Quick Start (DeepSeek)

1. Get your API Key from the [DeepSeek Platform](https://platform.deepseek.com)
2. Set `smartCommitMessage.apiKey` in VS Code Settings
3. DeepSeek's baseUrl and model are pre-configured by default — just click the sparkle button to use

## Commit Style Reference

- **conventional** — Follows the [Conventional Commits](https://www.conventionalcommits.org/) spec, e.g. `feat(scope): description`
- **simple** — One concise sentence describing the change
- **detailed** — Short summary + detailed change description

## Development & Release

```bash
git clone https://github.com/bin-ran/smart-commit-message.git
cd smart-commit-message
npm install
# Press F5 to launch Extension Host debugging
```

```bash
npm install -g @vscode/vsce
vsce package   # Package
vsce publish   # Publish
```

## License

MIT
