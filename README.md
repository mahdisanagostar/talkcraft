# Talkcraft

Standalone agent skill for planning, rewriting, auditing, and rehearsing high-stakes presentations with a framework inspired by Patrick Winston's presentation principles.

## Repository Layout

- `talkcraft/`
  Agent-facing skill folder.
- `talkcraft/scripts/audit_outline.py`
  Deterministic outline auditor.
- `talkcraft/references/`
  Framework notes, rubric, and host compatibility guidance.
- `talkcraft/assets/`
  Reusable briefing and rehearsal templates.

## Validation

```bash
python3 /Users/mahdi/.codex/skills/.system/skill-creator/scripts/quick_validate.py \
  /Users/mahdi/Desktop/git/talkcraft/talkcraft
python3 /Users/mahdi/Desktop/git/talkcraft/talkcraft/scripts/audit_outline.py \
  /Users/mahdi/Desktop/git/talkcraft/talkcraft/assets/presentation-brief-template.md
```

## Sync

Check Chef mirror drift:

```bash
python3 /Users/mahdi/Desktop/git/chef/adapters/shared/skills/talkcraft/scripts/sync_mirror.py \
  /Users/mahdi/Desktop/git/talkcraft/talkcraft --mode check
```

Repair drift from Chef copy:

```bash
python3 /Users/mahdi/Desktop/git/chef/adapters/shared/skills/talkcraft/scripts/sync_mirror.py \
  /Users/mahdi/Desktop/git/talkcraft/talkcraft --mode sync
```

## Notes

- The skill focuses on structure, delivery, narrative rhythm, and rehearsal discipline.
- It avoids copying any lecture transcript or protected wording.
- Chef can bundle the skill into both Codex and Claude runtimes.
