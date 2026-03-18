# obsidian skill

Claude Code skill for reading and writing notes in your [Obsidian](https://obsidian.md/) vault.

## What it does

Lets Claude create, read, search, and update Markdown notes in your Obsidian vault using standard file system operations. Includes templates for common note types (evergreen notes, how-tos, ADRs, MOC pages) and vault health checks.

## Installation

```bash
git clone git@github.com:zhrkvl/obsidian-skill.git ~/.claude/skills/obsidian
```

## Setup

Add your Obsidian vault path to your user-space `~/.claude/CLAUDE.md`:

```
OBSIDIAN_VAULT=/path/to/your/vault
```

The skill reads this variable to locate your vault. Without it, no vault operations will work.

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

## Default vault layout

Used for new vaults (respects existing structure if present):

```
00 Inbox/          # quick capture, unprocessed notes
10 Notes/          # evergreen, standalone notes
20 Projects/       # project-specific docs
90 Attachments/    # images, PDFs, diagrams
99 Meta/           # templates, MOC pages, glossary
```

## Limitations

- Operates via file system only — no Obsidian API or plugin integration
- Wikilink resolution is best-effort (no access to Obsidian's link index)
