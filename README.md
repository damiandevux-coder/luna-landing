# luna-landing

Marketing site for **Luna** — the AI Product Owner that lives in Slack (sprint health, backlog grooming, stakeholder briefs, blocker escalation).

Static HTML/CSS, no build step. Deploys to Vercel.

## Repo layout

| File | Purpose |
|------|---------|
| `index.html` | The full landing page |
| `style.css` | Design-token CSS system (Space Grotesk display font, layered-gradient hero) |
| `viktor-audit.md` | Competitor teardown of viktor.com — the positioning reference |
| `serve.ps1` | Local static server (gitignored; PowerShell, see below) |

## A/B test

Two versions are deployed from two branches:

| Branch | Version | Deploy |
|--------|---------|--------|
| `master` | **A** — V3.1 | https://po-agent-landing.vercel.app |
| `redesign-b` | **B** — V4 "out-execute" redesign | its own Vercel domain |

Strategy: *out-execute the clone* — keep Viktor's proven page structure but win on craft, copy, and Luna's vertical (product-owner) specificity. See `viktor-audit.md`.

## Local dev

This machine has no Node/Python on PATH. Serve statics with the PowerShell helper:

```powershell
./serve.ps1   # serves on http://localhost:5173
```

Sibling repos: [`luna`](https://github.com/damiandevux-coder/luna) (product) · [`luna-oauth`](https://github.com/damiandevux-coder/luna-oauth) (Slack OAuth service).
