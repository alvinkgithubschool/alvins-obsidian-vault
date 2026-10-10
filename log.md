---
type: log-pointer
date: 2026-09-08
tags: [type/log, ai-first: true]
---

# Vault Log Pointer

> **For future agent:** This file points to the daily log structure. All actual log entries live in `Logs/YYYY-MM-DD.md` files. This file explains the format.

---

## 📍 Log Location
All vault operation logs are stored in the `Logs/` folder.

## 📝 Daily Log Format
Each day has its own file: `Logs/YYYY-MM-DD.md`

### Frontmatter
```yaml
---
type: log
date: YYYY-MM-DD
tags: [type/log, ai-first: true]
---
```

### Entry Format
```markdown
**HH:MM** - action | description
```

### Example
```markdown
**08:00** - init | Vault initialized with _CLAUDE.md, index.md, Logs/
**08:15** - obsidian-save | Saved 3 decisions, 2 tasks, 1 person from conversation
**10:00** - obsidian-ingest | Ingested YouTube video: https://youtu.be/...
**22:00** - nightly | End of day: 5 tasks completed, 2 contradictions flagged, 1 synthesis created
```

---

## 🔗 Quick Links
- [[_CLAUDE.md]] - Configuration
- [[index.md]] - Vault catalog
- [[Logs/]] - All log files

---

## 📊 Today's Log
See: [[Logs/2026-09-08.md]]
