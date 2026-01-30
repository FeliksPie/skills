# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a collection of agent skills for Claude Code and agentskills.io-compatible agents. Skills provide specialized domain knowledge and frameworks for specific use cases (UX design, marketing, product strategy, etc.).

## Repository Structure

```
skills/
├── {skill-name}/
│   ├── SKILL.md           # Main skill file with YAML frontmatter + markdown instructions
│   └── references/        # Supporting reference files (optional)
│       └── *.md
└── README.md              # Skill catalog with descriptions and installation instructions
```

## Skill File Format

Each skill has a `SKILL.md` with this structure:

```markdown
---
name: skill-name
description: Brief description used for skill matching/discovery. Include trigger phrases.
---

# Skill Title

Main skill instructions in markdown...
```

The YAML frontmatter `description` field is critical for skill discovery - it should include keywords and trigger phrases that help match user requests to the skill.

## Adding New Skills

1. Create a new folder: `{skill-name}/`
2. Create `SKILL.md` with YAML frontmatter (`name`, `description`) and skill instructions
3. Optionally add `references/` folder with supporting `.md` files
4. Add the skill to `README.md` with description and example prompts

## Installation

Skills are installed via [skills.sh](https://skills.sh):
```bash
npx skills add wondelai/skills              # All skills
npx skills add wondelai/skills/{skill-name} # Individual skill
```

## Commit Policy

Commit directly to main.
