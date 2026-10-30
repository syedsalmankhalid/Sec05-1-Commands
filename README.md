# Sec05-1-Commands

A practice folder for learning Claude Code custom commands and skills. It holds one project-level skill and points to the user-level slash commands used alongside it.

## Contents

```
Sec05-1-Commands/
├── .claude/
│   └── skills/
│       └── weekly-update.md   # Skill: plain-language summary of the week's progress
└── README.md
```

## Skills and commands

**Project skill (in this folder)**

- `weekly-update` (`.claude/skills/weekly-update.md`): writes a short, three-paragraph summary of progress (features, fixes, docs). It works out the start date from the last update file, git history, or by asking, then groups the changes and writes them in plain language.

**User-level slash commands (in `C:\Users\HP\.claude\commands\`)**

These work in any project, not only this one.

- `/bug-scan [path]`: a read-only review of the project for bugs, missing error handling, and style inconsistencies, listed by severity.
- `/summarize-changes [path]`: summarizes what has changed since the last git commit. It needs a git repository.

## Usage

Start Claude Code in this folder:

```
claude
```

Then ask for a weekly update, or run a command:

```
/bug-scan
/summarize-changes
```

## Notes

- This folder is not yet a git repository. Run `git init` before using `/summarize-changes` here.
- The skills and commands are plain Markdown files with YAML frontmatter (the `---` block at the top) followed by instructions for Claude.
