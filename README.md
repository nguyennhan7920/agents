# agents

My Claude Code global config + installed skills/agents inventory.

## Global config

- **`AGENTS.md`** — source of truth for global agent instructions (tool preferences + machine tooling stack).
- **`CLAUDE.md`** — mirror of `AGENTS.md`. On my machine `~/.claude/CLAUDE.md` is a real symlink → `AGENTS.md`; committed here as a copy for portability.

Key rules in there: prefer `officecli` for all `.docx/.xlsx/.pptx` I/O (overrides skill python examples), prefer `lit` (liteparse) for PDF text extraction.

## Personal skills (`~/.claude/skills/`)

| Skill | Purpose |
|-------|---------|
| `effective-liteparse` | Local PDF/Office text extraction via `lit` CLI — parse-once-search-many discipline + BM25 `search.py` helper. |
| `officecli` | Create/read/inspect/modify `.docx/.xlsx/.pptx` via `officecli` single-binary CLI. |

## Installed plugins

Marketplaces: `claude-plugins-official` (anthropics/claude-plugins-official), `anthropic-agent-skills` (anthropics/skills), `claude-for-financial-services` (anthropics/financial-services).

### claude-plugins-official
| Plugin | Version |
|--------|---------|
| context7 | unknown |
| superpowers | 6.0.3 |
| discord | 0.0.4 |
| bigdata-com | 1.1.0 |
| desktop-commander | fea06819cb12 |
| github | unknown |

### anthropic-agent-skills
| Plugin | Version |
|--------|---------|
| document-skills | 35414756ca55 |
| example-skills | 35414756ca55 |
| claude-api | 35414756ca55 |

### claude-for-financial-services
| Plugin | Version |
|--------|---------|
| wealth-management | 0.1.2 |
| claude-for-msft-365-install | 0.1.6 |
| earnings-reviewer | 0.1.1 |
| equity-research | 0.1.2 |
| financial-analysis | 0.1.1 |
| fund-admin | 0.1.0 |
| gl-reconciler | 0.1.0 |
| investment-banking | 0.2.1 |
| kyc-screener | 0.1.0 |
| lseg | 1.0.0 |
| market-researcher | 0.1.1 |
| meeting-prep-agent | 0.1.1 |
| model-builder | 0.1.0 |
| month-end-closer | 0.1.0 |
| operations | 0.1.0 |
| pitch-agent | 0.1.1 |
| private-equity | 0.1.2 |
| sp-global | 1.0.1 |
| statement-auditor | 0.1.0 |
| valuation-reviewer | 0.1.1 |

## Installed agents (subagents)

From `claude-for-financial-services` plugins:

`earnings-reviewer`, `gl-reconciler`, `kyc-screener`, `market-researcher`, `meeting-prep-agent`, `model-builder`, `month-end-closer`, `pitch-agent`, `statement-auditor`, `valuation-reviewer`

_Inventory captured 2026-06-28._
