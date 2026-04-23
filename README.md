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
npx skills add interstitial-systems/skills --list

# Install only Planetary
npx skills add interstitial-systems/skills --skill planetary

# Install everything discovered under skills/
npx skills add interstitial-systems/skills
```

Install a single skill by path (sparse checkout):

```bash
npx skills add https://github.com/interstitial-systems/skills/tree/main/skills/planetary
```

### Claude Code (plugin marketplace)

This repo includes [`.claude-plugin/marketplace.json`](./.claude-plugin/marketplace.json) so you can add it as a marketplace, then install the bundled plugin (same pattern as [anthropics/skills](https://github.com/anthropics/skills)):

```text
/plugin marketplace add interstitial-systems/skills
```

Then browse plugins, choose **interstitial-skills** (marketplace) → **interstitial-skills** (plugin) → install. New skills under `skills/` should be listed in `marketplace.json` → `plugins[].skills` when you add them.

## Layout

| Path | Purpose |
| ---- | ------- |
| [`skills/`](./skills) | One folder per skill; each contains `SKILL.md`. |
| [`template/`](./template) | Starter `SKILL.md` for new skills. |
| [`.claude-plugin/`](./.claude-plugin) | Claude Code marketplace manifest (`marketplace.json`). |

## Spec

[Agent Skills specification](https://agentskills.io) · [skills.sh](https://skills.sh/)
