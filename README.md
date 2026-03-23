# 120-Day Renewal Cadence Tracker

A single-file web app for SaaS renewals managers to track accounts through a structured 120-day renewal pipeline. Built as a vibe coding exercise using Claude Code and reviewed with CodeRabbit.

## What It Does

Renewal managers lose deals not because of product — but because of timing and process gaps. This tracker gives a CSM or Renewals Manager a clear view of where each account sits across a 5-stage renewal cadence, from initial discovery at Day 120 through contract execution at Day 0.

**Features:**
- Account list with ARR and color-coded days-to-renewal badges (red / yellow / green)
- 5-stage 120-day renewal timeline with progress bar
- Stage status indicators: Complete, Active, Pending
- Summary card per account — ARR, days to expiry, AE owner, and champion
- Sample accounts: Chegg, Mercury, Groupon, Life360

**Renewal Stages:**
| Stage | Window | Focus |
|-------|--------|-------|
| 1 | Day 120–90 | Discovery & Baseline |
| 2 | Day 90–60 | Value Articulation |
| 3 | Day 60–30 | Commercial Alignment |
| 4 | Day 30–14 | Negotiation & Close |
| 5 | Day 14–0  | Signed & Transitioned |

## How to Run

No build tools or dependencies required. Just open the file:

```bash
open index.html
```

Or drag `index.html` into any browser. That's it.

## Tech Stack

- Vanilla HTML, CSS, JavaScript — fully self-contained
- Google Fonts (Space Mono) — only external dependency
- No frameworks, no bundler, no backend

## Built With

- **[Claude Code](https://claude.ai/code)** — AI coding assistant used to generate and iterate on the app
- **[CodeRabbit](https://coderabbit.ai)** — AI code review on the pull request

## CodeRabbit Review Experience

After pushing to a feature branch and opening a PR, CodeRabbit automatically reviewed the code within minutes. It flagged a legitimate security issue: `.claude/settings.local.json` had been accidentally committed, exposing an overly broad Bash permission (`git checkout:*`) that could allow arbitrary working-state rewrites.

**Fix applied:** Removed `.claude/` from version control and added it to `.gitignore`.

This was a real catch — the kind of misconfiguration that's easy to overlook in a manual review, especially when moving fast. It demonstrated exactly the value of automated AI review on every PR.

## Why This Project

Built as part of interview prep for a Renewals Manager role at CodeRabbit. The goal was to experience the product firsthand — using an AI code tool to build something relevant to the role, then letting CodeRabbit review the output the same way a real engineering team would use it.

The renewal cadence methodology mirrors real-world CSM practice: structured touchpoints, clear ownership, and stage-gated progression to protect ARR.
