# API 联通测试 Dashboard

[English](#english) | 简体中文

一个本地运行的 Web 工具，帮助开发者快速验证主流 LLM API 的连通性。浏览器里填写 API Key、选择服务商，即可一键完成两项核心测试：
- 获取可用模型列表
- 测量请求延迟（streaming TTFT + 总延迟）

整个过程不需要后端服务，所有 API 请求直接从你的浏览器发出。

🌐 **在线体验**: https://joker1point.github.io/api-dashboard/

## 功能特性

- **15+ 主流 LLM 服务商** — OpenAI、Anthropic、Google Gemini、DeepSeek、Moonshot、智谱、通义千问、SiliconFlow、Together AI、Groq、Mistral、零一万物、百川、MiniMax、Agnes AI
- **智能认证切换** — Anthropic 自动使用 `x-api-key` 请求头，其他使用 `Authorization: Bearer`
- **自定义 Base URL** — 不在列表里？手动填入即可
- **模型列表测试** — 拉取 `/v1/models` 端点
- **延迟测试** — streaming 模式测量 TTFT（首字时间）+ 总延迟
- **历史对比** — 多次测试结果对比，方便观察不同模型/时间的延迟差异
- **主题切换** — 亮色/暗色模式

## 在线使用

直接访问 https://joker1point.github.io/api-dashboard/，浏览器里填入 API Key 即可使用。

## 本地开发

```bash
npm install
npm run dev
# 访问 http://127.0.0.1:5173/
```

## 生产构建

```bash
npm run build
# 产物在 dist/ 目录
npm run preview
```

## 技术栈

- **React 18** + **Vite 5**
- **Ant Design 5** (含 ConfigProvider 主题系统)
- **Streaming Fetch** + `ReadableStream` API 测量延迟

## License

MIT

---

<a name="english"></a>
# API Connectivity Dashboard

A browser-based tool to verify LLM API connectivity. Fill in your API key, pick a provider, and instantly test:
- Model listing via `/v1/models`
- Streaming latency (TTFT + total)

No backend needed — all requests come from your browser.

🌐 **Live**: https://joker1point.github.io/api-dashboard/

## Features

- 15+ LLM providers (OpenAI, Anthropic, Gemini, DeepSeek, Moonshot, Zhipu, Qwen, etc.)
- Smart auth: `x-api-key` for Anthropic, `Bearer` for others
- Custom base URL support
- Latency history comparison
- Light/dark theme

## Quick Start

```bash
npm install
npm run dev
```

## License

MIT
