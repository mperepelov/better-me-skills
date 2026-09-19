# Better Me Skills

Reusable agent skills for maintaining useful project knowledge.

## Installation

With Node.js and npm installed, run this from your project directory:

```bash
npx skills@latest add mperepelov/better-me-skills
```

Choose the skills and coding agents you want to install them for.

To install only `knowledge-vault`:

```bash
npx skills@latest add mperepelov/better-me-skills --skill knowledge-vault
```

Add `--global` to make it available across projects, or `--agent codex` or
`--agent claude-code` to select an agent explicitly. For example:

```bash
npx skills@latest add mperepelov/better-me-skills --skill knowledge-vault --agent codex --global
```

Preview available skills without installing:

```bash
npx skills@latest add mperepelov/better-me-skills --list
```

## Available skills

| Skill | What it does |
| --- | --- |
| [knowledge-vault](skills/knowledge-vault/SKILL.md) | Finds and reads a project's knowledge vault or Markdown wiki, verifies current claims against project sources, and preserves durable knowledge when appropriate. |

## Using knowledge-vault

Ask your agent:

> Use knowledge-vault to find this project's wiki and read the context relevant
> to the work we're doing.

No separate setup skill is required. If you already have a wiki, provide its
path or reference it in your project's agent guidance. Otherwise, the skill asks
whether you want to create one. Obsidian is optional; an ordinary Markdown
directory works too.

The skill respects read-only and discussion-only requests. Creating a missing
vault requires your authorization.

## Updates

Update skills installed through the CLI when you want the latest versions:

```bash
npx skills@latest update
```

This command checks your installed skills, including those from other repositories.
