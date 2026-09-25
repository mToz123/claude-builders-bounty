# Bash guard hook

Stops a Claude Code shell call when the command is destructive. Safe commands pass through with exit 0.

## Install

```
mkdir -p ~/.claude/hooks && cp pre_tool_use.py ~/.claude/hooks/pre_tool_use.py
```

Point the Claude Code PreToolUse hook for Bash at that file. Blocked commands exit 2 and append one line to ~/.claude/hooks/blocked.log: time, project path, rule, command.

Blocked patterns: rm -rf, DROP TABLE, TRUNCATE, git push --force, and DELETE FROM with no WHERE. A normal command such as ls or git status is not logged.
