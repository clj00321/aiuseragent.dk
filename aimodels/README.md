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

> **Auto-generated from `aimodels.csv`** — Last updated: [auto-updated on CSV changes]

| | Provider | Chat URL (Deep Link) |
|:---:|---|---|
<!-- AUTO-GENERATED TABLE START -->
<!-- This section is automatically updated by GitHub Actions whenever aimodels.csv changes -->
<!-- DO NOT EDIT MANUALLY -->
<!-- AUTO-GENERATED TABLE END -->

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
