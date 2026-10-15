# Prompt for a fresh build session

Paste the following into the new session. The linked specification and public skill files contain the required context; no browser logins or approvals from the original conversation carry over.

---

Build the MVP described in:

https://github.com/kerbelp/project-directory-submissions/blob/main/docs/PRODUCT-SPEC.md

Read the complete spec and relevant repository instructions before implementation. Use these supporting sources:

- https://github.com/kerbelp/project-directory-submissions/blob/main/SKILL.md
- https://github.com/kerbelp/project-directory-submissions/blob/main/references/catalog.md
- https://github.com/kerbelp/project-directory-submissions/blob/main/assets/campaign-template.json
- https://github.com/kerbelp/project-directory-submissions/blob/main/assets/report-template.md
- https://github.com/kerbelp/project-directory-submissions/blob/main/references/example-report.md

The product is a paid assisted directory-submission service with customer and operator dashboards, a directory catalog, profile approvals, evidence, handoff tasks, and reports. Start with the operator-assisted workflow. Fully autonomous browser agents, MCP/plugins, inbox access, and platform purchasing of directory placements are deferred.

Build in a separate local application repository outside the Antaeus workspace and outside the public skill repository. Preserve the public skill as a reusable MIT project. Do not read/copy any Antaeus `.env`, use existing browser sessions, or import real customer data. Do not create a public application repo, deploy, send real emails, make real purchases, or submit any product to external directories as part of this build.

Use a small, maintainable stack with currently supported dependencies; document choices. Implement managed authentication, tenant checks, private evidence storage, relational migrations, and test-mode one-time service checkout. Support a local demo with fictional fixtures and mocked integrations if credentials are unavailable. Third-party directory fees remain separate and customer-paid; the app records approval/reservations/results, not customer card details.

Seed the catalog, including AI Collection with its affiliation disclosed. Verify current prices before any future real purchase; historical catalog observations are not checkout quotes. Keep the homepage as the primary submission URL. Distinguish receipt, review, scheduled launch, and verified live listing.

Work through the spec's build order and acceptance scenarios. Use ordinary implementation judgment and record assumptions rather than stopping for cosmetic decisions. Ask only for decisions that actually block implementation. Missing production pricing/legal/configuration is a production-launch blocker, not a local-development blocker.

Deliver the working application, setup/run instructions, migrations, fictional seeds, meaningful tests, and a demo of free and mixed campaigns including a human handoff and ambiguous payment. Report completed work, how to run it, validation evidence, and remaining production-launch decisions. Follow the application repository's review rules and keep unrelated repositories unchanged.

---

The original inbox screenshot is contextual evidence only. It is not a source of customer records or a fixture dataset. Nothing in this handoff authorizes external directory submissions or production deployment.
