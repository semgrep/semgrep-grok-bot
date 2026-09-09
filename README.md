# semgrep-grok-bot

**Semgrep Security Scanner** — a Grok Bot that scans code with Semgrep, triages findings, and helps fix them.

Share via Grok Bot team templates. Public listing: [x.ai/bot/marketplace](https://x.ai/bot/marketplace) (requires public-template enablement).

## Skills

| Skill | When |
| --- | --- |
| Getting started Semgrep Scanner | First run / how to use |
| Semgrep security scan | Scan a path, repo, or pasted files |
| Scan a pull request | PR URL or `owner/repo#n` |
| Triage Semgrep findings | Prioritize / false positives |
| Fix Semgrep findings | Remediate (cloud agent preferred) |
| Explain a Semgrep rule | Rule id meaning + safe fix |

## Memories (conventions)

- Severity counts first; findings as `path:line` + rule id; never invent CVEs
- Default rulesets: `p/security-audit` or `p/owasp-top-ten`
- Prefer fix over `nosemgrep`; justify suppressions
- No GitHub comments / pushes / PRs unless explicitly asked
- Concise engineering tone

## Routines

| Routine | Trigger |
| --- | --- |
| PR Semgrep scan — semgrep-grok-bot | `pr-opened` / `pr-pushed` on this repo |
| Weekday Semgrep ready-check | Weekdays 9:00 AM PT — alert only if Semgrep is broken |

## Integrations

- **Semgrep** (marketplace plugin `764`) — MCP + setup skill; CLI fallback
- **GitHub** — PR metadata / changed files for PR scans (add the GitHub connector)

## Local

```bash
git clone https://github.com/semgrep/semgrep-grok-bot.git
# Semgrep CLI optional if using the connector
semgrep --version
```
