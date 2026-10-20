---
name: project-directory-submissions
description: Research suitable product directories and launch platforms, prepare factual listing assets, submit free or approved paid listings, and track verified results. Use when asked to list a project on directories, find places to submit a startup or AI tool, or resume a listing campaign. Research-only requests do not authorize submissions.
---

# Project Directory Submissions

Help a project reach relevant audiences through accurate listings. Deliver verified links and an honest record of costs, publication states, and unfinished steps. Adapt the work to the request; a shortlist does not require a submission campaign.

## Establish scope and product facts

Infer research-only, preparation, submission, or resume mode from the request and existing records. Read an existing campaign before taking new action. Ask only for missing information that affects eligibility, truthful copy, spending, or the next required action; continue independent research meanwhile.

Build a compact product profile from the official website, documentation, public repository, supplied assets, and owner-confirmed facts:

- Name, canonical homepage, optional source repository and documentation links.
- What works today, audience, main use cases, maturity, pricing, and license where relevant.
- Tagline, short and long descriptions, categories, logo, and actual product screenshots.
- Approved business contact and account identity; founder/team/start-date/funding facts only when required and confirmed.
- Submission scope, total spending limit and currency, any per-site limits, selected paid destinations/plans, and excluded sites.

Use the homepage as the primary website URL unless the user chooses another destination or a platform requires a different kind of link. Keep source-code URLs in repository fields where supported. Do not silently substitute GitHub for the homepage. Do not invent traction, compliance, capabilities, dates, testimonials, or founder facts. Inspect imported/generated copy and images before saving them.

Keep campaign data in a private location chosen by the user or an ignored local folder such as `.listing-runs/<project>/`. Use [assets/campaign-template.json](assets/campaign-template.json) when a durable ledger is useful; it describes fields rather than requiring a particular tool or language. Never store credentials, session cookies, API keys, payment-card details, or token-bearing verification links. Public skill repositories contain reusable instructions and sanitized examples, not live account or campaign data.

## Find and qualify destinations

Read [references/catalog.md](references/catalog.md) and the relevant audience section of [additional directory candidates](references/directory-candidates.md) when discovering destinations. Together they provide 300+ research starting points. The machine-readable [candidate observations](references/directory-candidates.json) distinguish homepage observations from access-limited leads; neither establishes a tested submission workflow. Extend the catalog with relevant destinations from user-supplied lists, official search results, or comparable products' public listings. A supplied post is a research lead; verify its claims at the destination.

For shortlisted sites, check the current official submission flow or rules for:

- Audience and product eligibility, including restrictions on libraries, CLIs, open-source projects, or prelaunch products.
- Existing entries for the same product and homepage. Claim or update only the correct listing when authorized; do not overwrite a namesake or create avoidable duplicates.
- Cost, currency, billing cadence, upgrades, wait time, available launch dates, and publication conditions.
- Accounts, editorial review, required public fields, reciprocal badges/backlinks, generated-text restrictions, and automated-posting rules.

Classify cost as free, conditional-free, paid, or unknown. Free browsing or account creation does not prove free submission. A required backlink is conditional-free, and a discount is still paid. Explain meaningful conditions before committing. Do not add badges, edit the product website, enroll in newsletters, purchase upgrades, solicit votes, or send outreach unless authorized for that action.

Prioritize relevance and credible audience access, then effort, cost, and timing. Do not promise traffic, rankings, AI citations, or return on spend based on directory marketing claims. Apply the same criteria to maintainer-affiliated directories; disclose the relationship when recommending them. Skip poor fits rather than changing the product story to pass eligibility checks.

## Prepare and submit

Use available purpose-built tools or the user's requested browser, following the environment's tool instructions. Do not assume a particular browser API or connector is installed. Without external-write capability, deliver prepared fields, official submission links, and concrete handoffs instead of claiming submission.

Research and preparation alone do not authorize external publication. A request to submit free listings authorizes relevant ordinary free submissions within that scope. Inclusion of paid sites in a catalog does not authorize purchase. With no monetary authorization, keep spend at zero and present paid options for selection.

For paid submissions, establish the merchant/destination, selected plan, purpose, currency and spending ceiling before purchase. Account for taxes, fees, committed purchases, and recurring charges. An unused total budget is not permission to add a subscription or upgrade. Use current checkout terms and the tool's payment/confirmation requirements; prepare a reviewable checkout before any required approval. Distinguish advertised price, authorized ceiling, charged amount, and confirmed payment. Do not record an unpaid form as a completed paid submission.

Prepare required fields from the product profile, preserving meaning under character limits. Use relevant categories; leave optional private facts and marketing opt-ins blank unless requested. Keep showcases separate from sale offers. A personal login is not a claim that the person is the sole founder.

Continue through authorized steps without repeated permission requests. Preserve prior approvals for unchanged actions, while following action-time confirmations or handoffs required by the active tools. Hand off credential creation/reset, human-only posting, or other steps the agent cannot perform. If a site disallows generated text, leave that copy to the owner rather than providing an AI draft for them to paste. Explain site terms, CAPTCHA, or account problems specifically; do not invent a universal approval gate.

After each consequential step, inspect the resulting state. If validation fails, correct the identified problem and retry when safe. If a submit/payment action has an ambiguous outcome, check the receipt, account history, order state, or correct public listing before retrying. Do not risk a duplicate charge or listing. After a resolved validation retry fails for the same reason, record the blocker and continue elsewhere; revisit only with new evidence or user input.

Record the exact homepage URL submitted, supplementary repository URL, plan, status, timestamps, and evidence as progress changes. Keep evidence locally; avoid secret-bearing pages or redact them before sharing. Follow browser-tool requirements for screenshots and preserved handoff tabs.

## Verify, report, and resume

Use distinct states: `candidate`, `prepared`, `submitted`, `pending_review`, `scheduled`, `live`, `needs_user`, `blocked`, `rejected`, or `skipped`. A receipt establishes submission, not publication. Use `submitted` when only receipt is established, `pending_review` when review is explicit, and `scheduled` when a launch date is confirmed. Verify `live` on the correct public page; a preview, edit page, or predicted slug is insufficient. Track page availability separately when a public profile exists before its scheduled launch.

Keep observed public listing URLs separate from dashboard, receipt, and submission-form URLs. Do not invent public URLs. Record launch times with the platform timezone and, when useful, the user's timezone; use a calendar date even if no exact time is offered. Report unusually long queues and conditions that could later remove the listing or backlink.

Use [assets/report-template.md](assets/report-template.md) for the final report. Lead with verified counts by status and actual spend, followed by a compact table of destinations, links, status, cost, and next action. Prefer clickable public listing links. Label receipt, dashboard, and submit links when no public page exists. Keep sensitive account details, private evidence, and management links in the private ledger rather than a public/shareable report. Separate paid recommendations from completed purchases. A research-only result should compare candidates, observed costs, conditions, and sources without implying anything was submitted.

Read [references/example-report.md](references/example-report.md) for a fictional finished example. Keep the report proportional to the campaign; group skipped sites by reason when the list is long.

Before resuming, reconcile the ledger with visible receipts, public pages, and owner updates. Stale pricing or a scheduled date that has passed is not proof of current state. Do not duplicate completed work. Schedule future checks only when the user requests them and scheduling tools are available; otherwise report the next action without claiming monitoring exists.
