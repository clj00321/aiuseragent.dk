# AI Chat Prompt Deep Links

This folder contains `aimodels.csv` — a structured list of AI chat frontends that support
**prefilled prompt URL parameters** (also known as *chat launch parameters* or *prompt injection via query string*).

Each entry maps an AI provider to a direct deep link URL where a query string parameter
(`?q=`, `?prompt=`, etc.) pre-populates the chat input field on load.

---

## Data format

The CSV uses semicolon (`;`) as delimiter and has the following columns:

| Column | Description |
|---|---|
| `Ai-Developer` | Display name of the AI provider |
| `Ai-Chat Ikon` | URL to the provider's favicon or SimpleIcons SVG |
| `Ai-Chat Model` | Base URL with prompt parameter — append your prompt after the `=` |

---

## AI Chat Providers

| | Provider | Chat URL (Deep Link) |
|:---:|---|---|
| <img src="https://www.google.com/s2/favicons?domain=together.ai&sz=32" width="20" height="20"> | Together.ai | [https://chat.together.ai/?q=](https://chat.together.ai/?q=) |
| <img src="https://cdn.simpleicons.org/perplexity/1FB8CD" width="20" height="20"> | Perplexity.ai | [https://perplexity.ai/search?q=](https://perplexity.ai/search?q=) |
| <img src="https://cdn.simpleicons.org/x/000000" width="20" height="20"> | Grok.com | [https://grok.com/?q=](https://grok.com/?q=) |
| <img src="https://cdn.simpleicons.org/github/181717" width="20" height="20"> | Github.com | [https://github.com/copilot?prompt=](https://github.com/copilot?prompt=) |
| <img src="https://cdn.simpleicons.org/mistral/FF7000" width="20" height="20"> | Mistral.ai | [https://chat.mistral.ai/chat?q=](https://chat.mistral.ai/chat?q=) |
| <img src="https://cdn.simpleicons.org/meta/0082FB" width="20" height="20"> | Meta.ai | [https://meta.ai/?prompt=](https://meta.ai/?prompt=) |
| <img src="https://www.google.com/s2/favicons?domain=you.com&sz=32" width="20" height="20"> | You.com | [https://you.com/search/?q=](https://you.com/search/?q=) |
| <img src="https://www.google.com/s2/favicons?domain=kagi.com&sz=32" width="20" height="20"> | Kagi.com | [https://kagi.com/assistant?q=](https://kagi.com/assistant?q=) |
| <img src="https://www.google.com/s2/favicons?domain=app.blackbox.ai&sz=32" width="20" height="20"> | Blackbox.ai | [https://app.blackbox.ai/chat?q=](https://app.blackbox.ai/chat?q=) |
| <img src="https://cdn.simpleicons.org/huggingface/FFD21E" width="20" height="20"> | HuggingFace.co | [https://huggingface.co/chat/?prompt=](https://huggingface.co/chat/?prompt=) |
| <img src="https://www.google.com/s2/favicons?domain=consensus.app&sz=32" width="20" height="20"> | Consensus.app | [https://consensus.app/results/?q=](https://consensus.app/results/?q=) |
| <img src="https://cdn.simpleicons.org/openai/412991" width="20" height="20"> | ChatGPT.com | [https://chatgpt.com/?prompt=](https://chatgpt.com/?prompt=) |
| <img src="https://cdn.simpleicons.org/baidu/2932E1" width="20" height="20"> | Yiyan.Baidu.com | [https://yiyan.baidu.com/?q=](https://yiyan.baidu.com/?q=) |
| <img src="https://cdn.simpleicons.org/googlegemini/4285F4" width="20" height="20"> | Gemini.Google.com | [https://gemini.google.com/app?q=](https://gemini.google.com/app?q=) |
| <img src="https://cdn.simpleicons.org/anthropic/D97757" width="20" height="20"> | Claude.ai | [https://claude.ai/new?q=](https://claude.ai/new?q=) |
| <img src="https://www.google.com/s2/favicons?domain=andisearch.com&sz=32" width="20" height="20"> | AndiSearch.com | [https://andisearch.com/?q=](https://andisearch.com/?q=) |
| <img src="https://cdn.simpleicons.org/vercel/000000" width="20" height="20"> | V0.dev | [https://v0.dev/?q=](https://v0.dev/?q=) |
| <img src="https://cdn.simpleicons.org/alibaba/FF6A00" width="20" height="20"> | Tongyi.Aliyun.com | [https://tongyi.aliyun.com/qianwen/?q=](https://tongyi.aliyun.com/qianwen/?q=) |

---

## Usage

Append your URL-encoded prompt directly after the `=` in the deep link URL. Example:

```
https://claude.ai/new?q=Explain+quantum+entanglement+in+simple+terms
https://chatgpt.com/?prompt=Explain+quantum+entanglement+in+simple+terms
```

> **Note:** Not all platforms guarantee stable support for prompt pre-filling via URL parameters.
> Behaviour may change without notice as providers update their frontends.

---

## Icon sources

Icons are sourced from:
- [SimpleIcons](https://simpleicons.org/) — `https://cdn.simpleicons.org/{slug}/{hex-color}`
- [Google Favicons API](https://www.google.com/s2/favicons) — `?domain={domain}&sz=128`

---

*Part of the [AGILITY](https://github.com/clj00321/aiuseragent.dk) project — multi-LLM prompt launcher.*
