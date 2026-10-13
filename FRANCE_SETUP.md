# France-first setup (engineering, R&D, PhD/CIFRE)

This is a **public customization guide**, not a candidate profile. Keep personal information in a **local** `config/profile.yml` or a separate private workspace; never commit CVs, contact details, credentials, visa documents or application history to this public fork.

## Installation (local machine)
Prerequisite: Node.js 22.13+ (see `package.json`).

```bash
git clone https://github.com/yosri-ayari/career-ops.git
cd career-ops
npm install
npm run doctor
cp config/profile.example.yml config/profile.yml
cp templates/portals.example.yml portals.yml
```

Review and edit the two copied files **locally**. Use a supported AI CLI (e.g., Codex or Claude Code) for interactive evaluation. Playwright may need Chromium setup for PDF output.

## Two separate application tracks

**Industry / R&D** — ingénieur logiciel, ingénieur R&D, research software engineer, Python/Java backend, distributed systems, AI/ML, embedded systems and software testing.

**PhD / CIFRE** — doctorat, thèse, doctoral contract, CIFRE, software engineering, software analysis, software quality, applied AI and cyber-physical systems.

Hard constraints for both: jobs **in France**; no internships, apprenticeships, postdocs, or unrelated senior leadership roles. Confirm eligibility and funding for every PhD/CIFRE listing.

## Discovery sources
Use lawful public company-careers endpoints and any permitted ATS APIs/feeds supported by the scanner. For the research track, use ABG, CNRS, Inria, EURAXESS and ANRT listings/alerts with permitted ingestion, plus direct laboratory/doctoral-school sources. Do not assume that all of these portals have a public API or that their HTML scraping is authorized.

## Safe workflow
1. Scan permitted sources.
2. Verify whether a listing is still open.
3. Evaluate fit against a local/private CV, including missing required qualifications.
4. Draft truthful CV variants, cover letters and contact notes.
5. **Human reviews and submits**. Do not automate LinkedIn sessions, scraping, messaging or applications.

## Relationship to the separate job agent
The private `france-ai-job-agent` repository can remain the scheduler/collector. Career Ops can be the *local* evaluator and draft generator. A future adapter should pass sanitized vacancy JSON, not private CV data, between them.

## Current status
This guide does **not** enable France-specific scanners by itself or supply API keys. First test Career Ops locally with one manually supplied genuine French vacancy and check the output before integrating any scheduled collection.
