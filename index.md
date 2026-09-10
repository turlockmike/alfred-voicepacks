# alfred-voicepacks

Hand-authored loop doc (NOT memfs auto-render — that pipeline is orphaned
project-wide, see `~/architecture.md` invariant #11; this file states its
own content honestly instead of copying the stale "Auto-rendered by memfs"
banner other project index.md files still carry from before that broke).

**Scope:** storage + public-URL delivery for custom audio packs (TTS lines,
music clips) the household sends to the Dreame vacuum via `vac say`/`vac
play`. Files here are the packs themselves (tar.gz + .ogg); logic lives in
`~/.local/bin/vac`.

**Success:** a household member can ask for a voice line or music clip on
the vacuum and hear it play — met, shipped + verified 2026-09-10.

**Kill:** none active. Full status, open threads, next-action → `STATUS.md`.
