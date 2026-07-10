# luna-landing

Marketing site for **Luna** — the AI Product Owner that lives in Slack.

Sprint health, backlog grooming, stakeholder briefs, blocker escalation. She does the work, posts the result.

## Stack

Static HTML/CSS. No build step. Deploys to Vercel.

## Repo layout

| File | Purpose |
|------|---------|
| `index.html` | The full landing page |
| `style.css` | Design-token CSS system (Space Grotesk display font, layered-gradient hero) |
| `viktor-audit.md` | Competitor teardown of viktor.com — the positioning reference |

## Local dev

Any static server works. Examples:

```bash
# Python
python -m http.server 5173

# Node
npx serve .

# VS Code Live Server extension
```

Then open http://localhost:5173

## Deploy

```bash
npx vercel --prod
```

Live URL: https://po-agent-landing.vercel.app

## Sibling repos

- [`luna-oauth`](https://github.com/damiandevux-coder/luna-oauth) — Slack OAuth service
