# geno-meta

Meta-skills for the geno ecosystem — create, test, measure, and refine agent skills.

Built on the [Agent Skills](https://agentskills.io) standard. Includes Anthropic's [skill-creator](https://github.com/anthropics/skills/tree/main/skills/skill-creator) for the full create-test-measure-refine loop.

## Skills

| Skill | Description |
|-------|-------------|
| [skill-creator](skills/skill-creator/) | Create new skills, run evals, benchmark performance, optimize triggering |

## Install in Claude Code

```
/plugin install geno-meta@42euge/geno-meta
```

Or register as a marketplace:

```
/plugin marketplace add 42euge/geno-meta
```

## Creating a new skill

Use the `template/` directory as a starting point:

```
cp -r template/ skills/my-new-skill/
```

Then use the skill-creator to iterate:

> "Use the skill-creator to help me build a skill for X"

The skill-creator walks you through: draft → test → review → improve → repeat.

## Skill anatomy

```
skill-name/
├── SKILL.md          # Required: frontmatter + instructions
├── scripts/          # Executable code for deterministic tasks
├── references/       # Docs loaded into context as needed
└── assets/           # Templates, icons, fonts
```

## Attribution

The skill-creator skill is derived from [anthropics/skills](https://github.com/anthropics/skills) (Apache 2.0).
