# Evidence First Data Analysis — by The Ask Why Company

Analyze and validate datasets with reproducible, evidence-backed methods. Read-only by default; never fabricate metrics or perform data writes.

Read the skill: [skills/evidence-first-data-analysis/SKILL.md](skills/evidence-first-data-analysis/SKILL.md)

Works with Claude (Claude Code, Claude.ai) and any tool that reads the open [Agent Skills](https://agentskills.io) `SKILL.md` format.

## Install in Claude

**Claude Code:**
```
/plugin marketplace add theaskwhy/evidence-first-data-analysis
/plugin install evidence-first-data-analysis@evidence-first-data-analysis
```

Or from the full catalogue: `/plugin marketplace add theaskwhy/skills` then `/plugin install evidence-first-data-analysis@theaskwhy`.

**Manual:** copy `skills/evidence-first-data-analysis/` into `~/.claude/skills/` (personal) or `.claude/skills/` (project).

**Claude.ai:** zip the `skills/evidence-first-data-analysis` folder and upload it under Settings → Capabilities → Skills.

## Use with other AI agents

This skill uses the open **Agent Skills** standard. The same `SKILL.md` works with compatible tools including OpenAI Codex, Cursor, Gemini CLI, GitHub Copilot, Windsurf, Antigravity, OpenCode, and Goose.

**Quick install:** the open-source `skills` installer detects supported tools:
```
npx skills add theaskwhy/evidence-first-data-analysis
```

**Manual:** copy `skills/evidence-first-data-analysis/` into your tool's skills folder:

| Tool | Personal (all projects) | One project |
|---|---|---|
| Claude Code | `~/.claude/skills/` | `.claude/skills/` |
| OpenAI Codex | `~/.codex/skills/` | `.agents/skills/` |
| Cursor | `~/.cursor/skills/` | `.cursor/skills/` |
| Gemini CLI / Antigravity | `~/.gemini/skills/` | `.gemini/skills/` |
| GitHub Copilot | `~/.copilot/skills/` | `.github/skills/` |
| Windsurf | — | `.windsurf/skills/` |
| Any spec-compliant agent | — | `.agents/skills/` |

For tools without skills support, paste `SKILL.md` into the tool's rules or instructions file.

## Licence

MIT. See [LICENSE](LICENSE).
