# TalkCraft

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

All paths below are relative to the repository root.

```bash
python3 talkcraft/scripts/quick_validate.py
python3 talkcraft/scripts/audit_outline.py \
  talkcraft/assets/presentation-brief-template.md
```

## Sync

Check Chef mirror drift.
Default lookup uses sibling checkout:
`../chef/adapters/shared/skills/talkcraft`

```bash
python3 talkcraft/scripts/sync_mirror.py --mode check
```

Repair drift from Chef copy:

```bash
python3 talkcraft/scripts/sync_mirror.py --mode sync
```

If Chef lives elsewhere:

```bash
TALKCRAFT_MIRROR=path/to/chef/adapters/shared/skills/talkcraft \
  python3 talkcraft/scripts/sync_mirror.py --mode check
```

## Notes

- The skill focuses on structure, delivery, narrative rhythm, and rehearsal discipline.
- It avoids copying any lecture transcript or protected wording.
- Chef can bundle the skill into both Codex and Claude runtimes.
