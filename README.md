# Alexander Kadorkin

Technical product manager who builds. I design products and ship the tooling behind them: infrastructure automation, AI agents for operations, and field software.

## What I've built

**Infrastructure & AI operations** — a fleet of ~20 Linux servers (proxy/ingress nodes, Remnawave/Xray, Tailscale, HAProxy, CDN fronts) run mostly through AI-assisted tooling:

- [mia-assist](https://github.com/akadorkin/mia-assist) — MCP server + CLI to run a server fleet over SSH/Tailscale: status, audit, drift snapshots, two-step plan → apply actions with a journal.
- [mcp-remnawave](https://github.com/akadorkin/mcp-remnawave) — MCP server for the Remnawave panel (fork, v3 rework: safe edits with diff + confirm, backups, journal).
- [fleet-doctor](https://github.com/akadorkin/fleet-doctor) — AI on-call in Telegram: triages Grafana alerts, proposes a fix as a card with a confirm button, executes only allow-listed commands under a read-only / read-write policy.
- [server-code-graph](https://github.com/akadorkin/server-code-graph) — pull code and configs off servers, scrub secrets, build a knowledge graph to ask questions about the whole infrastructure.
- [claude-infra-skills](https://github.com/akadorkin/claude-infra-skills) — Claude Code skills distilled from real incidents: ingress migration under DPI, Tailscale peer relays, MTProto proxy fronts, CDN static mirrors.
- [remnanode-install-script](https://github.com/akadorkin/remnanode-install-script) · [vps-network-tuning-script](https://github.com/akadorkin/vps-network-tuning-script) — node bootstrap/hardening and network tuning.

**Industrial field software**

- **NFC Patrol** (private) — patrol control for process technologists at a building-materials (dry-mix) plant. Technologists tap NFC tags at checkpoints with an Android phone (PWA + TWA); every scan is stored on the device first, so a whole shift works offline, then syncs idempotently to the server. PostgreSQL is the source of truth; a Telegram bot sends a live log, missed-round and suspicious-scan alerts and end-of-shift XLSX reports to supervisors. Stack: React/Vite PWA, Web NFC, IndexedDB, FastAPI, PostgreSQL, Docker. **Status: integration testing on site.**

## Кратко по-русски

Технический продакт: проектирую продукты и сам делаю инструменты под них. Флот из ~20 серверов, которым управляю через MCP-инструменты и AI-дежурного; NFC Patrol — контроль обходов технологов по NFC-меткам для завода строительных смесей, сейчас на интеграционном тестировании.
