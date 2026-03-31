[job-hunter-os-README.md](https://github.com/user-attachments/files/26389654/job-hunter-os-README.md)
# Job Hunter OS

An AI-powered job search command center built as a single HTML file. No backend, no install, no accounts — open it in a browser and go.

Built by [Maria Fernanda Flores](https://fernanda-flva.github.io/portfolio/) for a Senior PM / Director-level search in NYC. Every module was designed around a real bottleneck in the application process.

---

## What it does

**Role Analyzer** — Paste a job description and get an ATS match score, H-1B signal, salary intelligence, and a breakdown of how well the role fits your profile before you invest time applying.

**Resume Tailor** — Takes your base resume and the JD, rewrites your bullets to match the role's language and priorities, outputs ATS-optimized copy.

**ATS Re-Scorer** — Re-scores your tailored resume against the JD so you can see exactly how much the needle moved.

**Cover Letter Generator** — Produces a targeted cover letter with full version history so you can compare iterations and roll back.

**Cold Outreach Module** — Drafts personalized outreach to hiring managers or referrals, with context carried forward from the role analysis.

**Application Tracker** — Tracks every application with status, notes, and the stored analysis from each prior step. Nothing needs to be re-entered.

Everything is stateful within a session — role analysis flows into resume tailoring flows into cover letter generation. No copy-pasting between tabs.

---

## Setup

**You need an Anthropic API key.** Get one at [console.anthropic.com](https://console.anthropic.com).

1. Download `index.html`
2. Open it in any browser (double-click, or `open index.html`)
3. Paste your API key in the field at the top — it starts with `sk-ant-`
4. Start with the Role Analyzer

Your key is stored in `localStorage` — it stays in your browser and never leaves your machine.

---

## Cost

Each module call is roughly $0.01–0.03 depending on resume/JD length. A full application cycle (analyze → tailor → cover letter → outreach) typically costs under $0.10.

---

## Stack

Vanilla JS · Single HTML file · Anthropic Claude API (claude-sonnet) · localStorage · No frameworks, no build step

---

## Notes

Built entirely with AI as a development collaborator. This was a deliberate constraint — the goal was to ship a working tool fast, using Claude as a coding partner, not just a writing assistant. The case study documenting the build process is [here](https://docs.google.com/document/d/1SOOqTA198j-ZbEpuwSx8sr-Yv-nwCIKEA7ryUVVRBRE/edit).
