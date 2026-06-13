# PHISHOPS

**Phishing Investigation Tracker — Part of [H3AD-OPS](https://h3ad-sec.github.io/H3AD-OPS/)**

PHISHOPS is a structured 7-step phishing investigation workflow tool for SOC analysts. Walk through each investigation phase, track findings per step, and get a live-aggregated IOC list — all in the browser, no backend required.

## Features

- 7-step investigation workflow: Receipt, Header Analysis, URL Triage, Sandbox, Identity Impact, Containment, Reporting
- Live IOC aggregator — pulls IPs, domains, URLs, and hashes from all step inputs automatically
- Step-by-step navigation with completion tracking
- Mode toggle: BYOK vs Managed
- localStorage persistence — resume investigations after page reload
- Fully responsive — works on mobile, tablet, and desktop

## Investigation Steps

| Step | Focus |
|------|-------|
| 1. Receipt | Email metadata, sender, recipients, subject, timestamps |
| 2. Header Analysis | Received chain, SPF/DKIM/DMARC, originating IP |
| 3. URL Triage | Link extraction, redirect chains, domain registration age |
| 4. Sandbox | Attachment detonation results, behavioral indicators |
| 5. Identity Impact | Okta/Azure AD activity, clicked users, credential exposure |
| 6. Containment | Blocked indicators, quarantined emails, user notifications |
| 7. Reporting | Summary, verdict, recommendations, ticket handoff |

## Live Tool

[h3ad-sec.github.io/PHISHOPS](https://h3ad-sec.github.io/PHISHOPS/)

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
| [H3AD-IR](https://h3ad-sec.github.io/H3AD-IR/) | PHISHBOOK |
| [H3AD-LEARN](https://h3ad-sec.github.io/H3AD-LEARN/) | Threat Hunting (9 ch), LOLBAS (8 ch) |
