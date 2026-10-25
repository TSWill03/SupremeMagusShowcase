# Supreme Magus — public QA status

Last verified: **2026-10-24**. Project: experimental magic-engine mod for **Minecraft Java 1.21.1 / NeoForge 21.1.x**.

## Demonstrated and validated locally
- Python automation: **35/35 PASS**.
- JUnit tests: **32/32 PASS**.
- NeoForge GameTestServer: **41/41 required tests PASS**, including server-side isolation for two FakePlayer identities; this is **not** two real authenticated network clients.
- In-game UI: H Arcane Workshop, K Grimoire, P Magical Training, Y ritual.
- A real cast of **Infero Menala Tak Gata** decreased mana HUD **100→92**, showed READY state and fire particles, corroborated by a screenshot-based verifier.
- Real screen footage recorded using OBS and reviewed from MP4 output; edited public video omits early personal screens and has **no audio**.

## Not yet validated
- Two authenticated Minecraft network sessions.
- Conventional dedicated server outside GameTestServer.
- Claims-provider compatibility, old-world save migrations and independent playerdata disk NBT audits.
- Shaders, Replay Mod, camera movements, different visual scales and locales.

This is a public **showcase of evidence**, not a declaration of release readiness or completeness. The mod's development repository is currently private. Nothing on this public page exposes private implementation code. GameTest result cards may be presented one at a time for video clarity; the one-second spacing is a **display delay**, not a claim of real per-test execution time. Individual GameTest names are reconstructed from annotated test declarations; their PASS refers to the NeoForge **aggregate batch** result, not a per-method runner log.

## Media
- `assets/demo.mp4` — selected 102-second Full HD edit, no audio.
- `assets/fire.png`, `assets/training.png` — gameplay screenshots.

All media from the isolated QA world. No filming of production server/player data. External project updates will be appended here as they are independently verified.

## 24 Oct 2026 — QA terminal with 1-second presentation delay (verified run)

- New public page: [test presentation](tests.html), with [edited OBS clip](assets/qa-terminal.mp4) (1:33, 1920×1080, no audio).
- The `minecraft_qa_showcase.py` presenter **runs real Python and Java test suites** then prints each measured result with `--delay 1`. For NeoForge GameTests, individual names are listed only after the official **41/41 required tests passed** batch marker, and explicitly displayed as `[BATCH PASS]`.
- Current Windows QA run: **35/35 pytest PASS**, **32/32 Java JUnit PASS**, **41/41 required NeoForge GameTests PASS**. Full JSON/console logs remain in the private QA worktree; results publicly reported without private code or user accounts.
- Gameplay smoke: world `New WorldQA_Supreme_`, held W for 1.1s, D for 0.8s, jumped, opened/closed creative inventory, toggled F5 and captured screenshots. Before/after world view clearly differs and [inventory screenshot](assets/inventory.png) verifies the E action. Not a multiplayer networking test.
- One user-authorized OBS recording `2026-10-24 21-32-48.mp4` (408.9s) was checked and stopped normally; master remains LOCAL because early frames include desktop windows, and the uploaded cut uses selected neutral-scene-only segments.
- **Not validated:** two distinct authenticated Minecraft clients, dedicated server networking, claims mods, legacy worlds, independent player NBT file audit, PT-BR and multiple display scales. The visual delay is a recording/presentation affordance, not test execution latency.
