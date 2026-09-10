# alfred-voicepacks — Status

**Status:** ACTIVE

Public GitHub repo (`turlockmike/alfred-voicepacks`) holding custom audio packs
for the household Dreame vacuum ("Sweeper", r9493h). `vac say TEXT` (edge-tts
→ OGG mono 16k, tar.gz'd as prompt 45) and `vac play FILE` (music, loudnorm)
push a pack here; the robot installs it from the *public* URL (LAN URL is
unreachable — Hyper-V firewall blocks inbound to this box). Shipped + verified
end-to-end 2026-09-10 (Beethoven clip + Hamlet TTS both played on the real
device, Mike confirmed). Only **one custom voice slot** exists on the robot
(T2 — installing a new pack overwrites the previous one; T3 slot doesn't
survive), so packs are transient by hardware design, not a growing library.

**Success** (met): Mike/Hilary/kids can ask for a voice line or music clip on
the vacuum and hear it play, via `vac say`/`vac play` — live capability, not
a one-off demo.

**Open thread:** two-way audio (Mike: "i'd love to talk to the vacuum") is
investigated and **blocked**, not solved — the device firmware requires a
pre-established Aliyun LinkVisual cloud session (SecurityGuard-encrypted
appKey/secret, mobile-app-only) before it accepts a STREAM_VIDEO/STREAM_AUDIO
MIoT action; the vendored library has no bypass (4 payload shapes tried
2026-09-10, all rejected code -1). Real next step — APK secret extraction —
is multi-session, out of heartbeat scope, not queued yet. Ground truth:
`~/resources/home/dreame-vacuum.md`.

**Kill condition:** none active — reopen this file only if the pack-storage
approach changes (e.g. a second voice slot becomes available, or the robot
gets LAN-reachable firmware) or if the intercom thread resumes.
