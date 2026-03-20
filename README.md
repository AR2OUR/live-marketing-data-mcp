# 📊 Live Marketing Data MCP

**Ask your AI about your real marketing data. No CSV exports. No tab switching. Just answers.**

> Connect Claude, Cursor, Windsurf and other AI assistants directly to your Meta Ads, Google Analytics 4, and Google Search Console accounts.

---

## 🔒 Security First — Built for Sensitive Data

Marketing data is sensitive. Your ad spend, ROAS, keyword rankings, and conversion data are things you don't want floating around in the cloud. That's exactly why this MCP was built to be **100% local**.

### Your data never leaves your machine

- **No cloud relay.** Every query goes directly from your AI client to the marketing platform APIs. There is no intermediary server, no data logging, no analytics on your queries.
- **Credentials are machine-locked, not just encrypted.** Your API tokens and service account keys are encrypted using a key derived from your specific machine's hardware identity. This means the encrypted files are **mathematically unreadable on any other computer** — even if someone copies them.
- **Credential files cannot be transferred.** If an attacker copies your credential files to another machine, they get useless ciphertext. Decryption requires the exact machine they were created on.
- **GA4 service account keys are encrypted on import.** The original JSON file is deleted immediately after encryption. Only the encrypted version is kept.
- **The server is a compiled binary.** No Python source is distributed, reducing the attack surface and preventing tampering.

This architecture was a deliberate design choice: the only way to guarantee your data stays private is to never move it. The MCP runs entirely on your hardware.

---

## ✨ What It Does

Instead of exporting data and pasting it into your AI, Live Marketing Data MCP lets your AI assistant query your actual accounts in real time:

```
You: "Which Meta campaign had the best ROAS last week?"
AI:  → fetches live data from your Meta Ads account
     → "Your Retargeting – Lookalike campaign had a 4.2x ROAS on $340 spend,
        outperforming your Awareness campaign (1.8x) by 133%."
```

```
You: "Compare organic traffic this month vs last month, broken down by source."
AI:  → queries your GA4 property directly
     → "Sessions are up 18% MoM. Direct traffic is flat, but organic search
        jumped 41% — your /blog/ai-tools page is driving most of the lift."
```

No copy-paste. No manual reports. Your AI becomes a live analytics co-pilot.

**Managing multiple clients?** Connect all your Meta Ads accounts, GA4 properties, and Search Console sites under one installation. Ask about a specific client by name or query all accounts at once — ideal for agencies running campaigns across multiple brands.

---

---

## 🚀 Quick Start

### 1. Download & Install

👉 **[Download Free Trial](https://github.com/AR2OUR/live-marketing-data-mcp/releases/tag/v1.0.0)**

Run `install.bat` — it handles everything in one go:
- Installs the server on your machine
- Launches the interactive setup wizard
- Connects your Meta Ads, GA4, and Search Console accounts
- Auto-detects and configures all your installed AI platforms

No separate steps. Run once, you're set up.

### 2. Start Asking Questions

Restart your AI client and start querying:

```
"What was my total Meta ad spend this week?"
"Show me my top 5 landing pages by sessions this month"
"Which keywords am I ranking in positions 4-10 that I could push to top 3?"
"Compare my campaign performance this month vs last month"
"Generate a full performance report for Nike for October"
```

---

## 🖥️ Supported Platforms

| Platform | Status |
|----------|--------|
| Claude Desktop | ✅ Supported |
| Cursor | ✅ Supported |
| Windsurf | ✅ Supported |
| Cline (VS Code) | ✅ Supported |
| Continue | ✅ Supported |
| Antigravity (Google) | ✅ Supported |

The setup wizard auto-detects which platforms you have installed and configures all of them simultaneously.

---

## ⚙️ Manual Config (Advanced)

If you prefer to configure manually, add this to your platform's MCP config file:

**Claude Desktop** (`%APPDATA%\Claude\claude_desktop_config.json`):
```json
{
  "mcpServers": {
    "live-marketing-data": {
      "command": "C:\\path\\to\\live-marketing-data-mcp.exe",
      "args": []
    }
  }
}
```

**Cursor** (`%APPDATA%\Cursor\User\globalStorage\cursor.settings\mcp.json`):
```json
{
  "mcp": {
    "live-marketing-data": {
      "command": "C:\\path\\to\\live-marketing-data-mcp.exe",
      "args": []
    }
  }
}
```

---

## 💰 Pricing

| Plan | Price | Includes |
|------|-------|----------|
| **Free Trial** | $0 | 10 tool calls to explore the product |
| **Pro** | **$49 one-time** | Unlimited calls, all 6 tools, all platforms, lifetime access |

No subscriptions. Pay once, use forever.

👉 **[Get Pro — $49 lifetime](https://promptflowpro.lemonsqueezy.com/checkout/buy/ba7396ee-5291-4b82-855b-4beedfe7862e?enabled=1416338)**

---

## 🔑 License Activation

After purchase, activate your Pro license directly in your AI chat:

```
"activate license YOUR-LICENSE-KEY-HERE"
```

Or re-run `install.bat` and select the license activation option from the setup wizard.

---

## 🐛 Troubleshooting

**Tools not appearing in Claude?**
→ Make sure you restarted Claude Desktop after setup. The installer writes to both the standard and Windows Store install paths automatically.

**Meta Ads showing no accounts?**
→ Your token needs `ads_read` permission. Re-generate your token in Meta Business Manager with that scope.

**Need to update credentials or add a new account?**
→ Re-run `install.bat` — the setup wizard lets you update any connection.

For support: **support@promptflow.digital**

---

## 📦 About

Built by [PromptFlow](https://promptflow.digital) — tools that make AI assistants genuinely useful for marketers and agencies.

- Website: [promptflow.digital](https://promptflow.digital)
- Support: support@promptflow.digital
- Platform: Windows (macOS/Linux coming soon)
