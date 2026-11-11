# App Documentation Builder

**Turn a codebase or app idea into documentation people can actually use.**

A reusable AI prompt and portable skill for creating public descriptions, technical fact sheets, product requirements, developer guides, launch checklists, and handoff documentation.

Created by [William Lodge](https://williamlodge.com) · [MIT license](LICENSE)

## Start here

### Use the prompt
Open [the master prompt](prompts/app-documentation-builder.md), copy it into your preferred AI assistant, and add your project name and available repository, website, or notes.

```text
Project: My app
Sources: This repository and the existing docs directory
Mode: Create the full documentation package
Output: Markdown under docs/, with a linked index
Public audience: Overview and marketing copy only
```

Give the assistant access only to sources you intend it to inspect. Without repository access, it will produce a partial package and identify what remains unknown. This project requires no API key or runtime dependency; your chosen assistant may have its own requirements.

### Use the skill
The portable skill lives in [skills/app-documentation-builder](skills/app-documentation-builder/SKILL.md). Its folder contains SKILL.md and optional UI metadata under agents/.

For an agent that supports SKILL.md, add that entire folder through its supported skill installation mechanism. Installing this repository does not automatically install a skill in ChatGPT or any other product. Installation steps and invocation syntax vary by host.

In a compatible host, try:

```text
Use $app-documentation-builder to document this application.
Inspect the code first and distinguish implemented, tested,
deployed, planned, and unknown behavior.
```

For hosts without skill support, use the standalone prompt.

## What it creates

| Area | Documentation |
|---|---|
| Identity | App overview, tagline, audience, purpose |
| Public copy | Short descriptions, website copy, store listing draft |
| Product | Business brief, feature inventory, roles, journeys, PRD |
| Engineering | Technical sheet, architecture, database/API reference, setup |
| Operations | Deployment, backups, monitoring, security and privacy |
| Experience | Design system, user help, admin guide |
| Launch | Testing evidence, readiness checklist, roadmap, changelog |
| Continuity | Ownership register, developer and AI handoff |

All 18 documentation sections are specified in the prompt and skill. Small projects can combine related sections into fewer files.

## Designed to keep claims honest

- Implementation, verification, and deployment are separate facts.
- Unknown details stay unknown instead of becoming plausible fiction.
- Technical claims point back to evidence.
- Public descriptions and internal operational details stay separate.
- Secrets and personal records do not belong in generated documentation.
- Proposed policy language is not a compliance certification.
- Existing documentation can be updated in place.

This is an instruction package, not a scanner or autonomous documentation service. Results depend on the assistant, available evidence, and review. Generated documents still need human review before publication.

## Examples

**Existing app:** “Document this repository. Produce public descriptions and internal developer documentation. Mark every unverified claim.”

**New idea:** “Create a proposed documentation package from these notes. No application exists yet. Mark technical choices and features as proposed.”

**Update:** “Refresh the existing docs against the current code. Preserve valid material, identify outdated claims, and summarize changes.”

**Handoff:** “Produce the developer overview, technical sheet, setup guide, and AI handoff only. Include the coverage matrix and explain what is out of scope.”

## Contributing

Improvements to clarity, evidence handling, and documentation coverage are welcome. Open an issue or pull request with a concrete example. Use fictional or redacted projects; never submit credentials or private customer data.

## License

MIT — Copyright (c) 2026 William Lodge LLC.
