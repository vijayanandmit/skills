# Skills

Reusable skills for finance, investing, research, and decision support.

This repository supports two layouts:

- Codex-compatible standalone skill folders at the repo root.
- Claude Code marketplace plugin package under `plugins/market-skills/`.

## Available Skills

| Skill | Purpose |
|---|---|
| `stock-analyst` | Actionable stock, ETF, sector, and market recommendations with risk controls. |
| `earnings-call-analyst` | Analyze earnings releases, call transcripts, guidance, and management tone. |
| `etf-comparison` | Compare ETFs by exposure, fees, liquidity, performance, tax fit, and portfolio role. |
| `market-news-screener` | Screen current market news for catalysts, risks, and tradeable implications. |
| `options-trade-planner` | Plan defined-risk options trades with entry, exit, Greeks, and scenario checks. |
| `portfolio-risk-review` | Review portfolio concentration, drawdown risk, factor exposure, and rebalancing actions. |
| `sector-rotation-screener` | Identify stronger and weaker sectors using momentum, valuation, macro, and sentiment. |

Each skill lives in its own folder with a required `SKILL.md` and optional `agents/openai.yaml` metadata.

## Codex Layout

```text
skill-name/
  SKILL.md
  agents/
    openai.yaml
```

## Claude Code Layout

```text
.claude-plugin/
  marketplace.json
plugins/
  market-skills/
    .claude-plugin/
      plugin.json
    skills/
      skill-name/
        SKILL.md
```

## Codex Usage

Install or copy the individual skill folders you want to use. Skills are intentionally independent, so consumers can take one skill without pulling the full collection.

## Claude Code Usage

Add this repository as a Claude Code plugin marketplace:

```text
/plugin marketplace add vijayanandmit/skills
```

Then install the plugin:

```text
/plugin install market-skills@vijay-skills
```

After install, restart Claude Code or run:

```text
/reload-plugins
```

Plugin skills are namespaced. Example:

```text
/market-skills:stock-analyst Analyze NVDA with current data, entry zone, target, stop-loss, confidence, and risk.
```
