# Token Guard 💰

[🇺🇸 English](./README.md)

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blue)](https://clawdhub.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](./SKILL.md)

## 别让 AI 睡觉的时候烧你的钱。

> Agent 7×24 跑着，Opus $75/百万 token。算算账吧。

有人一个任务花了 $55（注册邮箱+X账号）。有人第一周探索就烧了 $100+。Token Guard 帮你盯着账单。

## 快速开始

```bash
# 当前用量 + 成本
bash scripts/token-guard.sh status

# 设置每日 $10 预算
bash scripts/token-guard.sh set-budget 10

# 硬限制：超预算自动降级到 Haiku
bash scripts/token-guard.sh set-budget 10 80 true claude-haiku-3-5

# 跑之前先估算
bash scripts/token-guard.sh estimate claude-opus-4 50000 10000

# 历史用量
bash scripts/token-guard.sh history
```

## 功能

- **预算预警** — 80% 提醒，100% 报警
- **自动降级** — 超预算自动切便宜模型
- **成本预估** — 跑贵任务前先算一算
- **用量历史** — 按天按模型看明细
- **模型对比** — 一眼看出哪个贵哪个便宜

## 真实省钱效果

| 改什么 | 月省多少 |
|---|---|
| sub-agent 改用 Haiku | ~70% |
| heartbeat 改用 Flash | ~95% |
| 设每日预算 + 自动降级 | 防止账单爆炸 |
| heartbeat 调到 55 分钟（卡缓存窗口） | ~30% |

## 依赖

- `bash` 4+, `python3`, `curl`

## 相关项目

- [config-guard](https://github.com/jzOcb/config-guard) — 配置验证和自动回滚
- [upgrade-guard](https://github.com/jzOcb/upgrade-guard) — 安全升级 + watchdog
- [agent-guardrails](https://github.com/jzOcb/agent-guardrails) — AI agent 代码行为约束

## 许可

MIT
