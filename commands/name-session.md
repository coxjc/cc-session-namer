---
description: Name this session now from the whole conversation, replacing any current name
allowed-tools: Bash(bash:*)
---

The session-namer plugin was just asked to name this session. Its output:

```
!`bash "${CLAUDE_PLUGIN_ROOT}/hooks/rename-session.sh" --force "${CLAUDE_SESSION_ID}"`
```

Relay that outcome to the user in one short line and do nothing else. Do not
run any tools. If the output starts with `named:`, tell them the new name. If
it is empty, say the plugin gave no output and suggest setting
`SESSION_NAMER_DEBUG=1` and reading `$TMPDIR/session-namer.log`.
