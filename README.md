# claude-site-audit

> A Claude Code plugin that audits websites for SEO, accessibility, GEO, and AI search readiness — and generates a client-ready PDF report.

## Plugin Installation (Claude Plugin Directory)

Once listed in the Claude plugin directory:
```bash
claude plugin install claude-site-audit@claude-community
```

Commands will be available as `/claude-site-audit:site-audit`.

## Manual Install

```bash
# Clone into your Claude config directory
git clone https://github.com/rjspence3/claude-site-audit ~/.claude/plugins/claude-site-audit

# Copy command
cp ~/.claude/plugins/claude-site-audit/.claude/commands/site-audit.md ~/.claude/commands/
```

Command is available immediately in Claude Code as `/site-audit`.

## What it does

`/site-audit` audits public-facing websites across four dimensions:

- **Accessibility** — ADA/WCAG compliance signals
- **SEO** — Search engine optimization fundamentals
- **GEO** — Generative Engine Optimization (AI search readiness)
- **Usability** — Mobile, navigation, contact info, online services

It evaluates 17 checks, assigns a letter grade, and produces a **client-ready PDF report** with a scorecard and prioritized fix recommendations.

### Organization types supported

`municipality`, `library`, `tourism`, `utility`, `restaurant`, `museum`, `housing`, `general`

The "why it matters" framing and compliance angle are tailored to the org type.

## Modes

**Single audit:** Provide one URL — get one PDF report.

**Batch audit:** Provide a list of URLs (CSV, spreadsheet, or plain list) — get one PDF per site plus a summary spreadsheet with all scores and grades.

## Usage

```
/site-audit
```

Claude will ask for:
1. URL(s) to audit
2. Organization name(s)
3. Organization type(s)

Or provide them directly:

```
/site-audit https://example.com "City of Springfield" municipality
```

## Requirements

This skill references companion files for check criteria, scoring methodology, and a PDF generation script. The full skill bundle is at `~/.claude/skills/site-audit/` if you're using this as part of a larger Claude setup.

---

Built by [Rob Spence](https://nomouthlabs.com). MIT License.
