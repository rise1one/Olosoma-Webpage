# OloSoma Website - Workflow Guide

**Repository**: https://github.com/rise1one/Olosoma-Webpage
**Owner**: Diogo (rise1one)
**Assistant**: Claude (Opus 4.5)

---

## Session Commands

### `START SESSION`
When user says **START SESSION**, Claude will:
1. Read `WORKFLOW.md` to check last session status
2. Read `SESSIONS.md` for context on previous work
3. Check `PROGRESS.md` for pending tasks
4. Review any uncommitted changes (`git status`)
5. Present summary of where we left off
6. Ask what to work on OR continue pending tasks

### `CLOSE SESSION`
When user says **CLOSE SESSION**, Claude will:
1. Summarize all work completed this session
2. List all files created/modified
3. Update `SESSIONS.md` with session log entry
4. Update `LATEST_CHANGES.md` if significant changes made
5. Update `PROGRESS.md` if tasks completed
6. Stage and commit all changes to git
7. Push to GitHub repository
8. Confirm session closed with next steps

---

## Current Status

**Last Session**: Session 1 - December 16, 2025
**Status**: CLOSED
**Last Commit**: `[Session 1] Initial setup - workflow established, session tracking created`

### Pending Tasks
- [ ] Install dependencies (`npm install`)
- [ ] Run dev server and test current site
- [ ] Determine edits/improvements to make
- [ ] Begin development work

### Next Session Should
- Start with `START SESSION`
- Install dependencies and run dev server
- Decide what to edit/improve on the website

---

## Session Log Summary

| Session | Date | Summary | Status |
|---------|------|---------|--------|
| 1 | Dec 16, 2025 | Initial setup, repo created, workflow established | Closed |

---

## File Responsibilities

| File | Updated When |
|------|--------------|
| `WORKFLOW.md` | Session status changes, workflow updates |
| `SESSIONS.md` | Every session close (detailed log) |
| `PROGRESS.md` | Tasks completed or added |
| `LATEST_CHANGES.md` | Significant code changes |
| `WORK_SUMMARY.md` | Major project state changes |

---

## Git Commit Convention

Format: `[Session X] Brief description`

Examples:
- `[Session 1] Initial setup and workflow`
- `[Session 2] Updated hero section styling`
- `[Session 3] Fixed mobile navigation bug`

---

## Quick Commands Reference

```bash
# Development
npm install          # Install dependencies (first time)
npm run dev          # Start dev server
npm run build        # Production build test

# Git (handled by Claude on CLOSE SESSION)
git add .
git commit -m "[Session X] message"
git push origin main
```

---

## Notes

- All edits tracked per session
- Nothing pushed until session closes
- Can abandon changes if needed (before CLOSE SESSION)
- Always review summary before confirming close

---

*Workflow Version: 1.0*
*Created: December 16, 2025*
