# obsidian skill

Claude Code skill for reading and writing notes in your [Obsidian](https://obsidian.md/) vault.

## What it does

Lets Claude create, read, search, and update Markdown notes in your Obsidian vault using standard file system operations. Includes templates for common note types (evergreen notes, how-tos, ADRs, MOC pages) and vault health checks.

## Installation

```bash
git clone git@github.com:zhrkvl/obsidian-skill.git ~/.claude/skills/obsidian
```

## Setup

Add your Obsidian vault path to your user-space as ENV variable:
```
OBSIDIAN_VAULT=/path/to/your/vault
```

Or just in plain text in `~/.claude/CLAUDE.md` like
```
My obsidian vault is located at "/path/to/the/vault".
```

Without it, no vault operations will work.

## Usage

Invoke directly or describe what you need:

```
/obsidian create a note about X
```

```
search my notes for Y
```

```
document this in obsidian
```

The skill triggers automatically on phrases like "create a note", "add to vault", "search my notes", "new obsidian page", etc.

## Limitations

- Operates via file system only — no Obsidian API or plugin integration
- Wikilink resolution is best-effort (no access to Obsidian's link index)
