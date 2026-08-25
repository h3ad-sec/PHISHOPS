# PHISHOPS

**Phishing Investigation Tracker — Part of [H3AD-OPS](https://h3ad-sec.github.io/H3AD-OPS/)**

PHISHOPS is a phishing investigation tool for SOC analysts, in two modes: a guided 7-step manual tracker, and an automated scanner that parses a raw EML file and scores it against live threat intelligence. Both run entirely in the browser, no backend required.

## Features

- **Manual Tracker**: 7-step investigation workflow, Triage, Header Analysis, URL Triage, Attachment Sandbox, Identity/Okta Impact, Containment, and Closure, each with its own fields, checklist, and escalation criteria
- **Auto Scan**: drop a raw .eml file or paste email text, headers/URLs/attachment SHA256 hashes are extracted client-side, forwarded phishing reports are unwrapped automatically, then every indicator is enriched via VirusTotal, URLScan, and RDAP with a computed 0-100 risk score
- **Overview view**: a landing page on both modes explaining how to use PHISHOPS, its capabilities, and how to read results, alongside the working tool
- Live IOC aggregator (manual mode) — pulls senders, IPs, URLs, hashes, C2 indicators, and affected users from all step inputs automatically
- Key import for Auto Scan's VirusTotal/URLScan keys from a JSON, TXT, CSV, or Markdown file
- Export: copy IOCs, copy the full report, or download it as a Markdown file
- localStorage persistence — resume manual investigations after page reload
- Fully responsive — works on mobile, tablet, and desktop

## Investigation Steps (Manual Tracker)

| Step | Focus |
|------|-------|
| 1. Triage | Alert source, envelope fields, sender/reply-to/return-path mismatch |
| 2. Header Analysis | Received chain, SPF/DKIM/DMARC, originating IP |
| 3. URL Triage | Link extraction, redirect chains, domain registration age |
| 4. Attachment | File hash, sandbox detonation, C2 indicators |
| 5. Identity | Okta/Azure AD activity, clicked users, credential exposure |
| 6. Containment | Blocking, revocation, evidence preservation |
| 7. Closure | Root cause, disposition, IOC handoff for downstream TI |

## Live Tool

[h3ad-sec.github.io/PHISHOPS](https://h3ad-sec.github.io/PHISHOPS/) (Manual Tracker) &middot; [Auto Scan](https://h3ad-sec.github.io/PHISHOPS/auto.html)

## Part of H3AD-SEC

PHISHOPS is a sub-tool under [H3AD-OPS](https://h3ad-sec.github.io/H3AD-OPS/), the SOC operations hub of the [H3AD-SEC](https://h3ad-sec.github.io) platform.


## H3AD-SEC Platform Modules

| Module | Tools |
|--------|-------|
| [H3AD-X](https://h3ad-sec.github.io/H3AD-X/) | X-VERDIKT, PARSE-X, DNSCOPE, MAILSCOPE |
| [H3AD-AI](https://h3ad-sec.github.io/H3AD-AI/) | INSIGHT-AI, QUERYCRAFT-AI, FPLENS-AI, ATTMAP-AI, CHRONO-AI, MALBRIEF-AI, PROMPTVAULT |
| [H3AD-DETECT](https://h3ad-sec.github.io/H3AD-DETECT/) | TRACERULES |
| [H3AD-HUNT](https://h3ad-sec.github.io/H3AD-HUNT/) | HYPOS, PIVEX, TRACEPULSE |
| [H3AD-OPS](https://h3ad-sec.github.io/H3AD-OPS/) | QUICKTRACE, SHIFTLOG, PHISHOPS |
| [H3AD-DF](https://h3ad-sec.github.io/H3AD-DF/) | REGSCOPE, MALBRIEF-AI |
| [H3AD-IR](https://h3ad-sec.github.io/H3AD-IR/) | Coming soon |
| [H3AD-LEARN](https://h3ad-sec.github.io/H3AD-LEARN/) | Threat Hunting (9 ch), LOLBAS (8 ch) |
