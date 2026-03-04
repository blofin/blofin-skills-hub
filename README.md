# BloFin Skills Hub

AI agent skills for [BloFin](https://blofin.com), powered by [blofin-mcp](https://www.npmjs.com/package/blofin-mcp).

## Install

Install all skills:

```bash
npx skills add https://github.com/blofin/blofin-skills-hub
```

Install a specific skill:

```bash
npx skills add https://github.com/blofin/blofin-skills-hub --skill blofin-trader
```

Or paste the GitHub URL into your agent's chat:

```
https://github.com/blofin/blofin-skills-hub
```

> First time? Run the **blofin-setup** skill to configure your API keys and MCP server.

## Skills

| Skill | Description |
|-------|-------------|
| [blofin-setup](skills/blofin-setup/) | MCP server setup and API key configuration |
| [blofin-market-data](skills/blofin-market-data/) | Prices, orderbook, candlesticks, funding rates (no auth) |
| [blofin-account-manager](skills/blofin-account-manager/) | Balances, positions, leverage, margin mode |
| [blofin-trader](skills/blofin-trader/) | Order placement, TP/SL, algo orders, batch ops |
| [blofin-portfolio-analyst](skills/blofin-portfolio-analyst/) | PnL analysis, trade history, performance reports |
| [blofin-risk-manager](skills/blofin-risk-manager/) | Position sizing, liquidation monitoring, risk scoring |
| [blofin-funding-monitor](skills/blofin-funding-monitor/) | Funding rate monitoring and market sentiment analysis |
| [blofin-asset-manager](skills/blofin-asset-manager/) | Fund transfers, deposit/withdrawal tracking |
| [blofin-copy-trading](skills/blofin-copy-trading/) | Copy trading and lead trader management |

## Contributing

We welcome community contributions! To add your own skill:

1. **Fork** this repo and create a branch: `git checkout -b feature/<skill-name>`
2. Create a folder under `skills/` with a `SKILL.md` file (see existing skills as reference)
3. Submit a **Pull Request** to `main`

### SKILL.md Format

```markdown
---
name: your-skill-name
description: "What it does"
version: 1.0.0
license: MIT
metadata:
  openclaw:
    emoji: "🔧"
    requires:
      bins:
        - node
      env:
        - BLOFIN_API_KEY
        - BLOFIN_API_SECRET
        - BLOFIN_PASSPHRASE
    primaryEnv: BLOFIN_API_KEY
auto_activate:
  - "trigger phrase"
---

# Your Skill Name

[Instructions, workflows, example prompts, safety rules]
```

## Links

- [BloFin API Docs](https://docs.blofin.com/index.html)
- [blofin-mcp](https://www.npmjs.com/package/blofin-mcp)

## License

MIT
