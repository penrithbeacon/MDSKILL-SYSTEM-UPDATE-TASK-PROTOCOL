# SYSTEM — Update Task Protocol (UT S)

**MD Skill UUID:** `45d49924-2169-4510-b88f-53e53c0261d4`
**Package ID:** `com.penrithbeacon.mdskills.system-update-task-protocol`
**Version:** 1.4.0
**Type:** procedural
**Author:** Anthony Harrison
**Author Email:** widgets@penrithbeacon.com
**License:** MIT
**Homepage:** https://openaiskillpackage.com/
**Tags:** system, protocol, task-master, cudi, aistarter

App-owned session protocol for the Update Task CUDI flow

---

## Synopsis

Defines the exact sequence of API calls the AI must make to read and revise an existing task's record through the app's own API instead of editing any file directly.

This is one of the 9 fixed SYSTEM protocol skills Cup and Ring AI Browser requires -- one per
CUDI slot (task Create/Update/Delete/Implement, macro Create/Update/Delete/Implement, and Ad
Hoc Session) -- bundled together by the `AISTARTER-SYSTEM` starter package so a fresh project
can have all 9 imported and assigned to their slots in one action, rather than dragged in
individually. Split out of Task Master's own built-in `system-skills.js` so each one has a
real, independently verifiable identity through the Cup and Ring Registry -- the same skill,
not a copy or a sample.

---

## How It Works (Behavior)

Injected automatically, first, at the start of every matching CUDI session, before any other
configured skill. Defines the exact sequence of API calls the AI agent must make against the
host application's own local API to record/progress the session -- never edits application
data directly, and never carries out the work described by the task/macro itself. See
`SKILL.md` for the full call sequence.

---

## What's in this .mdskill package?

```
skill/
├── manifest.yaml     — identity, version, declared (empty) capabilities/permissions
├── SYSTEM.md          — fixed, byte-identical verification protocol (same as every .aiskill)
├── SKILL.md            — the actual skill (fixed entry filename, same convention as .aiskill)
├── CARD.md            — human-facing summary, generated from manifest.yaml
├── README.md          — this file (byte-identical to the repo root copy)
├── CHANGELOG.md
├── LICENSE.txt
└── checksums.yaml     — SHA-256 of every file above
```

No `assets/`, no `inputs/` — an `.mdskill` package is inert by nature.

---

## License

MIT — see `LICENSE.txt`.
