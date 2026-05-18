# AGENTS.md - JC-Skills

Personal OpenCode skills collection. Each skill is a self-contained instruction file that OpenCode loads via the `skill` tool.

## Repo Structure

```
skills/<skill-name>/SKILL.md    ← each skill is exactly this path
```

- No build system, no tests, no CI. This is a content-only repo.

## Skill File Format

Every `SKILL.md` MUST use YAML frontmatter with at minimum:
- `name` — kebab-case identifier matching the directory name
- `description` — what triggers the skill (single sentence)

Standard optional fields: `version`, `tags`, `language`, `author`, `license`.

## Adding a Skill

1. Create `skills/<skill-name>/SKILL.md`
2. The directory name should match the `name` in frontmatter (kebab-case)
3. Write detailed instructions in Chinese (this repo's convention)
4. OpenCode discovers skills from the `available_skills` list — no registration step needed beyond creating the file

## Existing Skills

| Skill | Purpose |
|---|---|
| `codex-token-summary` | Statistics for local Codex token usage from `~/.codex/` state DB + rollouts |
| `project-sess-summary` | Project session memory management using `jcemb` vector tool |

## Gotchas

- `project-sess-summary` references an external CLI tool `jcemb` that must be installed separately (`jcemb scan`, `jcemb query`).
- `codex-token-summary` reads from `~/.codex/state_*.sqlite` — only works on machines with Codex installed.
- Skills use `zh-CN` as the default language. Keep all skill content in Chinese unless there's a specific reason to use English.
