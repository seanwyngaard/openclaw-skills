# OpenClaw Income Skills

11 production-ready skills for [OpenClaw](https://openclaw.ai) and [Claude Code](https://claude.ai/code) built on the [Agent Skills](https://agentskills.io) open standard.

## Skills

### Tier 1 — Win Work, Deliver Work, Manage Clients

| Skill | What It Does |
|-------|-------------|
| [freelance-proposal-engine](skills/freelance-proposal-engine/) | Analyzes job listings and generates tailored, high-converting proposals for Upwork/Fiverr/Freelancer |
| [seo-content-factory](skills/seo-content-factory/) | End-to-end SEO pipeline: keyword research → competitor SERP analysis → fully optimized article |
| [client-project-manager](skills/client-project-manager/) | Full freelance CRM: track clients, projects, invoices, weekly updates, payment reminders |

### Tier 2 — Scale Your Services

| Skill | What It Does |
|-------|-------------|
| [web-scraper-as-a-service](skills/web-scraper-as-a-service/) | Generates complete scraper code + clean data + client-ready documentation package |
| [landing-page-generator](skills/landing-page-generator/) | Creates responsive, conversion-optimized landing pages from a brief — single HTML file, no dependencies |
| [email-sequence-builder](skills/email-sequence-builder/) | Builds complete email sequences (welcome, sales, nurture, re-engagement, abandoned cart) with A/B subject lines |
| [social-media-content-calendar](skills/social-media-content-calendar/) | Platform-adapted content calendars with hashtags and image prompts, exportable to Buffer/Hootsuite/Later |

### Tier 3 — Niche Services

| Skill | What It Does |
|-------|-------------|
| [resume-and-cover-letter](skills/resume-and-cover-letter/) | ATS-optimized resumes and tailored cover letters matched to specific job descriptions |
| [technical-doc-generator](skills/technical-doc-generator/) | Scans codebases and generates API docs, READMEs, architecture diagrams, and onboarding guides |
| [competitor-analysis-report](skills/competitor-analysis-report/) | Professional competitive analysis with SWOT, feature matrix, pricing comparison, and strategic recommendations |
| [contract-generator](skills/contract-generator/) | Freelance contracts, SOWs, NDAs, and retainer agreements — customizable templates |

## Installation

### Claude Code

```bash
# Single skill
cp -r skills/freelance-proposal-engine ~/.claude/skills/

# All skills
cp -r skills/* ~/.claude/skills/
```

Or point Claude Code at this repo:

```bash
claude --add-dir /path/to/openclaw-skills/skills
```

### OpenClaw (ClawHub)

```bash
clawhub install freelance-proposal-engine
clawhub install seo-content-factory
# etc.
```

## Usage

Each skill is invoked as a slash command:

```
/freelance-proposal-engine "Need a React developer to build a dashboard, $3k budget, 4 weeks"

/seo-content-factory "best CRM for small business" 2000

/client-project-manager add client "Acme Corp" --contact "jane@acme.com" --rate "$100/hr"

/landing-page-generator "AI writing tool, $19/mo, free trial, targeting content marketers"

/email-sequence-builder welcome "Online fitness coaching, $49/mo subscription"
```

See each skill's `SKILL.md` for full documentation and examples.

## Skill Format

Each skill follows the Agent Skills standard:

```
skill-name/
  SKILL.md    # YAML frontmatter + markdown instructions
```

The `SKILL.md` has two parts:
- **Frontmatter** (between `---`): name, description, allowed tools, configuration
- **Body**: Instructions the AI follows when the skill is invoked

## Contributing

PRs welcome. To add a skill:

1. Create a new folder under `skills/` with your skill name
2. Add a `SKILL.md` following the format above
3. Test it locally with Claude Code or OpenClaw
4. Open a PR with a description of what the skill does

## License

[MIT](LICENSE)
