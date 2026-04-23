# Interstitial skills

Public **Agent Skills** for **Interstitial** products and workflows. Each skill is a self-contained folder with a `SKILL.md` (YAML frontmatter + instructions). Layout matches common multi-skill repos such as [anthropics/skills](https://github.com/anthropics/skills): browse [`./skills`](./skills) for what ships here.

The main application code may live in private repos; this repository is the **public** catalog for installable skills only.

## Skills

| Skill | Folder | Summary |
| ----- | ------ | ------- |
| **planetary** | [`skills/planetary`](./skills/planetary) | Interstitial **Planetary Software** — one HTTP MCP URL (`POST /api/v1/atlas/mcp`), four tools for environmental / sensor data. |

Add new rows here when you add folders under `skills/`.

## Install

Uses the [Vercel skills CLI](https://github.com/vercel-labs/skills) (OpenCode, Claude Code, Cursor, and [many other agents](https://github.com/vercel-labs/skills#supported-agents)).

```bash
# List skills in this repo
npx skills add interstitial-wg/skills --list

# Install only Planetary
npx skills add interstitial-wg/skills --skill planetary

# Install everything discovered under skills/
npx skills add interstitial-wg/skills
```

Install a single skill by path (sparse checkout):

```bash
npx skills add https://github.com/interstitial-wg/skills/tree/main/skills/planetary
```

## Layout

| Path | Purpose |
| ---- | ------- |
| [`skills/`](./skills) | One folder per skill; each contains `SKILL.md`. |
| [`template/`](./template) | Starter `SKILL.md` for new skills. |

## Spec

[Agent Skills specification](https://agentskills.io) · [skills.sh](https://skills.sh/)
