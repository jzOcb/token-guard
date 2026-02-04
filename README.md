# Token Guard 💰

[🇨🇳 中文文档](./README_CN.md)

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blue)](https://clawdhub.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](./SKILL.md)

## Stop burning money while you sleep.

> Your agent runs 24/7. Opus costs $75/M tokens. Do the math.

One user spent $55 on a single task (registering an email + X account). Another burned $100 in a week just exploring. Token Guard watches your spend so you don't have to.

## Quick Start

```bash
# Current usage + costs
bash scripts/token-guard.sh status

# Set $10/day budget
bash scripts/token-guard.sh set-budget 10

# Hard limit: auto-downgrade to Haiku when exceeded
bash scripts/token-guard.sh set-budget 10 80 true claude-haiku-3-5

# Estimate before running
bash scripts/token-guard.sh estimate claude-opus-4 50000 10000

# Usage history
bash scripts/token-guard.sh history
```

## Features

- **Budget alerts** — warning at 80%, critical at 100%
- **Auto-downgrade** — hit budget → auto-switch to cheaper model
- **Cost estimation** — estimate before running expensive tasks
- **Usage history** — daily breakdown by model
- **Model comparison** — see real cost differences at a glance

## The Real Savings

| What you change | Monthly savings |
|---|---|
| Route subagents to Haiku | ~70% |
| Route heartbeat to Flash | ~95% |
| Set daily budget + downgrade | prevents blowouts |
| Cache-aware heartbeat (55min) | ~30% |

## Requirements

- `bash` 4+, `python3`, `curl`

## Related

- [config-guard](https://github.com/jzOcb/config-guard) — Config validation and auto-rollback
- [upgrade-guard](https://github.com/jzOcb/upgrade-guard) — Safe upgrades with snapshot and watchdog
- [agent-guardrails](https://github.com/jzOcb/agent-guardrails) — Code-level enforcement for AI agents

## License

MIT
