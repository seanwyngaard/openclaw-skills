# OpenClaw Skills Landscape & Income Opportunity Analysis

> Research conducted: 13 February 2026
> Target income: $1,000 - $2,000/month

---

## What is OpenClaw?

**OpenClaw** is a free, open-source autonomous AI agent created by Peter Steinberger. It runs locally on your machine and uses LLMs to execute real-world tasks, with messaging platforms (WhatsApp, Telegram, etc.) as its primary UI. Steinberger describes it as "an AI that actually does things."

### Name History
| Date | Name | Reason for Change |
|------|------|-------------------|
| Late 2025 | **Clawd** | Original name, lobster theme |
| Jan 27, 2026 | **Moltbot** | Anthropic sent trademark notice ("Clawd" too close to "Claude") |
| Jan 30, 2026 | **OpenClaw** | Permanent identity for enterprise adoption, emphasizes open-source |

### Key Facts
- **ClawHub** (public skill registry): 5,705+ community-built skills as of Feb 7, 2026
- Skills follow the [Agent Skills](https://agentskills.io) open standard (same as Claude Code)
- Skills are just a folder with a `SKILL.md` file + optional scripts/references
- CLI: `clawhub install <slug>`, `clawhub update --all`, `clawhub sync --all`

### OpenClaw vs Claude Code
They are **different tools** serving different purposes:
- **Claude Code**: AI coding assistant (CLI for software development)
- **OpenClaw**: Autonomous AI agent (runs tasks via messaging platforms)
- Both use the same **Agent Skills** standard for skill format
- Skills can be cross-compatible between the two platforms

---

## Existing Skills Ecosystem (What's Already Out There)

### ClawHub Registry Categories (5,705+ skills)

| Category | Count | Income Relevance |
|----------|-------|-----------------|
| AI & LLMs | 287 | Medium |
| Search & Research | 253 | Medium |
| DevOps & Cloud | 212 | High |
| Web & Frontend Development | 202 | High |
| Marketing & Sales | 143 | **High** |
| Browser & Automation | 139 | **High** |
| Productivity & Tasks | 135 | Medium |
| Coding Agents & IDEs | 133 | Medium |
| Communication | 132 | Medium |
| CLI Utilities | 129 | Low |
| Notes & PKM | 100 | Low |
| Media & Streaming | 80 | Low |
| Transportation | 73 | Low |
| Git & GitHub | 66 | Medium |
| Smart Home & IoT | 56 | Low |
| Health & Fitness | 55 | Low |
| Shopping & E-commerce | 51 | **High** |
| Calendar & Scheduling | 50 | Low |
| Data & Analytics | 46 | High |
| Finance | 22 | **High** |

### Notable Income-Related Skills Already Available

#### Agent Marketplaces
- **ClawdGigs** - "The Upwork for AI agents" - register and manage your agent profile
- **ClaWork** - Job board for AI agents
- Multiple agent-to-agent protocol skills for marketplace participation

#### Claude Code Ecosystem (Compatible Skills)
- **Ralph Wiggum Marketer** - Autonomous AI copywriter with market research
- **Claude Code PM** / **RIPER Workflow** / **Claude Task Master** - Project management
- **Book Factory** - Content creation
- **Trail of Bits Security Skills** - Security auditing
- **Claude Command Suite** - 148+ slash commands, 54 AI agents
- **wshobson/commands** - 57 production-ready slash commands (15 workflows, 42 tools)
- **Invoice Organizer** - Auto-organizes invoices/receipts for tax prep
- **PRD Generator** - Product Requirements Documents from context
- **Web Assets Generator** - Generate web assets
- **n8n_agent** - n8n workflow automation integration

### Proven Income Strategies Already Documented

Sources: [OpenClaw Money Making Guides](https://openclawmoney.com/), [5 OpenClaw Automations That Make Money](https://markaicode.com/openclaw-money-making-automations-2026/), [5 Profitable Business Ideas](https://superframeworks.com/articles/openclaw-business-ideas-indie-hackers)

| Strategy | Estimated Income | Barrier to Entry |
|----------|-----------------|-----------------|
| SEO content writing | $150-1,000/day (3-5 posts/day at $50-200/post) | Low |
| Web scraping services (Upwork) | $1,000-8,000/month ($200-2,000/project) | Medium |
| Freelance services via Fiverr/Upwork | $500-2,000/month within 3 months | Low |
| Selling skills on ClawHub | $10-200/skill | Medium |
| Email marketing copy | Variable | Low |

---

## Claude Code Skills Format Reference

Since we'll be writing skills compatible with both Claude Code and OpenClaw:

### Minimum Skill Structure
```
my-skill/
  SKILL.md           # Required - YAML frontmatter + instructions
  scripts/           # Optional - executable scripts
  references/        # Optional - supporting docs
  examples/          # Optional - example outputs
```

### SKILL.md Format
```yaml
---
name: skill-name
description: What this skill does and when to use it
disable-model-invocation: false    # true = manual /invoke only
user-invocable: true               # false = background knowledge only
allowed-tools: Read, Grep, Bash    # restrict tool access
context: fork                      # run in isolated subagent
agent: Explore                     # subagent type (Explore, Plan, general-purpose)
---

# Skill Name

Instructions for Claude/OpenClaw go here.

## Usage
Examples of how to use this skill.

## Additional resources
- For details, see [reference.md](reference.md)
```

### Key Features
- `$ARGUMENTS` - access user input
- `$ARGUMENTS[0]`, `$0` - positional args
- `` !`command` `` - dynamic context injection (runs shell before prompt)
- `${CLAUDE_SESSION_ID}` - session tracking
- String substitutions for dynamic content

### Skill Locations
| Scope | Path |
|-------|------|
| Personal | `~/.claude/skills/<name>/SKILL.md` |
| Project | `.claude/skills/<name>/SKILL.md` |
| Plugin | `<plugin>/skills/<name>/SKILL.md` |
| OpenClaw | `~/.openclaw/skills/<name>/SKILL.md` |

---

## Sources

- [VoltAgent/awesome-openclaw-skills](https://github.com/VoltAgent/awesome-openclaw-skills) - Curated OpenClaw skills collection
- [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) - Claude Code skills/plugins list
- [OpenClaw Complete Guide 2026](https://www.nxcode.io/resources/news/openclaw-complete-guide-2026)
- [Claude Code Skills Docs](https://code.claude.com/docs/en/skills)
- [OpenClaw Skills Docs](https://docs.openclaw.ai/tools/skills)
- [ClawHub Registry](https://clawhub.ai/skills)
- [OpenClaw Money Making Guides](https://openclawmoney.com/)
- [33 OpenClaw Automations (Medium)](https://medium.com/@rentierdigital/33-openclaw-automations-you-can-set-up-in-30-minutes-that-start-making-you-money-tonight-f8c3b8a402f1)
- [5 OpenClaw Money Automations 2026](https://markaicode.com/openclaw-money-making-automations-2026/)
- [5 Profitable OpenClaw Business Ideas](https://superframeworks.com/articles/openclaw-business-ideas-indie-hackers)
- [wshobson/commands](https://github.com/wshobson/commands) - 57 production-ready slash commands
- [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) - Claude Code skills collection
- [BankrBot/openclaw-skills](https://github.com/BankrBot/openclaw-skills) - Crypto/DeFi/trading skills
- [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) - Curated Claude skills
- [Upwork: OpenClaw/Claude Code jobs](https://www.upwork.com/freelance-jobs/apply/open-claw-Claude-code-N8N-automation-engineer_~022019554254063986089/)
- [OpenClaw Wikipedia](https://en.wikipedia.org/wiki/OpenClaw)
