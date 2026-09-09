# semgrep-grok-bot

Grok Bot template: **Semgrep Security Scanner** — scan code for security issues with Semgrep and share via Grok Bot team templates ([marketplace](https://x.ai/bot/marketplace)).

## What it does

- Runs Semgrep (CLI or Semgrep connector) on a path, repo, PR, or pasted files
- Ranks findings by severity with file/line evidence
- Redacts secrets in reports
- Offers triage / fix follow-ups (no push without an explicit ask)

## Bot package

Marketplace/team share is a Grok Bot template:

| Piece | Role |
| --- | --- |
| Profile | Storefront name + short description |
| Skill | `semgrep-security-scan` — how to run and report a scan |
| Plugin | Semgrep (`764`) — MCP + setup skill |
| Memory | Scan conventions (ruleset defaults, no invented findings) |

## Local setup on this machine

Semgrep CLI is expected on PATH (`semgrep`). Optional: add the Semgrep Grok Bot / Cursor connector for MCP scanning.

## Status

Built for team template sharing first. Public marketplace publish depends on account enablement.
