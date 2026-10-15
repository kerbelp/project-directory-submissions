# Listing Campaigns — product specification

Version 0.1 · October 15, 2026 · Working product name; branding is undecided.

This is a build brief for a separate application. The public `project-directory-submissions` repository remains the reusable MIT-licensed skill and source of workflow examples. Do not turn it into the application repository.

## 1. Product and business model

Help founders get their projects into relevant directories through a paid, assisted submission campaign. Customers supply product facts, approve destinations, complete account/payment handoffs, and receive a report of verified results. An operator performs research and authorized submission work, assisted by the existing skill and whatever tools are available.

Initial buyer: a founder launching one SaaS product, AI application, open-source project, or developer tool. Agencies managing multiple products are a later audience. The core job is: “Get my project submitted to suitable places, keep my spending under control, and show me what actually happened.”

Commercial structure:

- Free public skill for people who want to do the work themselves.
- Fixed service fee per campaign, collected on the product website.
- Third-party directory fees paid separately by the customer directly to the directory.
- No mandatory AI Collection purchase, automatic promotion bundle, or guaranteed acceptance, backlinks, rankings, traffic, or revenue.

Build the paid-service workflow, but use payment test mode until the owner approves the offer, price, campaign scope, turnaround promise, cancellation/refund policy, and legal pages. These are launch decisions, not reasons to block local development. The admin-configured offer must specify the included submission-attempt limit; it must not advertise “unlimited submissions.” Save the purchased offer as an immutable snapshot on the campaign.

## 2. MVP boundary

The MVP is an operational concierge product with customer and operator dashboards. It is useful without browser automation or an LLM integration.

Included:

- Authentication, one owner per customer workspace, multiple projects and campaigns.
- Editable product profiles and approved visual assets.
- Directory catalog seeded from the public skill, including free, conditional-free, paid, and unknown-cost options.
- An operator-created shortlist with official sources, fit reasons, current cost observations, and customer approval.
- Submission records, evidence, customer handoff tasks, launch dates, and manual publication verification.
- One-time service checkout, payment reconciliation, private reports, and downloadable exports.
- Operator console with audited access to assigned campaigns and catalog maintenance.

Deferred:

- Autonomous browser agents, stored customer sessions, remote browser sharing, automatic account creation, CAPTCHA solving, and password management.
- Platform purchasing or reselling directory placements, customer budget wallets, subscriptions, and agency/team billing.
- Gmail ingestion, broad inbox access, bulk outreach, voting, automatic website badges, or unsolicited reminders.
- Public report hosting/share links, referral commissions, and a comprehensive directory database.
- Public Claude/Codex plugin submissions, MCP integration, continuous monitoring, and LLM-generated copy.

Free and paid directories are first-class in the MVP. Paid-directory execution uses a customer payment handoff; a stored campaign budget does not mean the platform holds or spends those funds.

## 3. End-to-end journey

1. Visitor sees the offer, the process, an example report, and the distinction between the service fee and directory fees. No unsupported ROI claims.
2. Customer signs in, creates a project, enters a homepage and product facts, and uploads logo/screenshots. Optional copy assistance can come later; manual entry works now.
3. Customer creates a draft campaign and chooses free-only or free-and-paid research. Third-party spend defaults to zero. They enter exclusions and choose whether conditional backlink listings may be proposed.
4. Customer purchases the configured service offer on the website. The server confirms payment through a verified payment-provider event; a success redirect alone does not unlock paid fulfillment.
5. Assigned operator reviews the facts and creates a shortlist within the offer's attempt limit. Customer can answer missing factual questions before approving the campaign.
6. Customer approves the product-profile revision and selected destinations. Each selection identifies the URL to submit, known conditions, and any spend authorization. Approval has a timestamp and is inspectable later.
7. Operator completes authorized work in an external browser. For customer-only logins, passwords, verification, required agreements, payment, or human-authored posts, create a task with the exact site, reason, safe URL, and next step. Customer uses their own browser; the app never requests their password, cookie, OTP, or card number.
8. Operator records the observed result and evidence. Customer-provided updates remain labelled as owner-reported until verified. Uncertain payment/submission outcomes are reconciled before any retry.
9. Customer sees a private report with public listing links where verified, clearly labelled receipts where appropriate, statuses, costs, launch dates, and unresolved tasks.
10. Operator marks execution delivered only when each selected destination has a recorded outcome or an explicit unresolved handoff the customer accepts as part of delivery. Review and launch can remain pending; delivery never implies publication. Customer can close the campaign or purchase another campaign later.

Do not require a fresh purchase merely to view or export a previously delivered campaign. A cancelled campaign stops new operator work; retain its history and explain any already-completed external actions. Handle refunds separately from cancellation because externally submitted listings cannot necessarily be undone.

## 4. User-facing screens

| Screen | Essential content and actions |
| --- | --- |
| Landing / offer | Outcome, process, service scope/price when configured, sample report, free skill link, exclusions, separate directory fees, affiliation disclosure. |
| Projects | Customer's projects, create project, active campaign summaries. |
| Product profile | Homepage/repository/docs, factual descriptions, business contact, maturity/pricing/license, source notes, approved assets, revision review. |
| Campaign setup | Offer snapshot, free-only/paid research, directory budget, exclusions, conditional-link preference, checkout state. |
| Shortlist review | Fit reason, official source/check date, cost class/plan/cadence, publication conditions, selected checkbox, submitted homepage, affiliation badge, approval action. |
| Campaign dashboard | Counts by status, clear “waiting on you” tasks, selected destinations, evidence indicators, cost totals, planned launches. |
| Entry detail | Field values submitted, history, exact observed status, public/receipt links labelled separately, payment uncertainty, evidence, next action. |
| Handoff task | Exact destination and action, why customer is needed, official safe URL, mark done/decline with non-secret note or evidence. Completion triggers review, not an automatic live status. |
| Report | Status summary, linked results table, separate spending totals, next actions, export controls, last verification times. |
| Operator console | Assigned work, missing facts, stale quotes, uncertain outcomes, evidence review, manual verification and delivery. |
| Catalog admin | Create/edit/archive directories, sources, eligibility, cost observations, affiliation, check date. Preserve historical campaign snapshots. |

Use plain language. For example, “Received; awaiting review” instead of a generic green “Success.” Show launch dates with the platform timezone and the customer's selected IANA timezone. Unknown price and unknown payment must never display as $0. A public profile that exists before launch can be linked while the row remains Scheduled.

## 5. Directory discovery and selection

Seed all 22 destinations from [the catalog](../references/catalog.md), preserving the difference between observed pilot routes and unverified candidates. The Markdown catalog is a starting point; import it into structured seed data for the application. Do not scrape private accounts or use campaign screenshots as seed data.

Each directory stores official homepage/submission/rules links, audience tags, eligibility notes, cost class, plan observations, reciprocal-link requirements, automation/generated-text restrictions, verification date, and affiliation.

Ranking is understandable: product fit and eligibility first, then cost, effort, timing, and customer preference. No invented numeric quality scores or assumed traffic. MVP recommendations are operator-curated; automated ranking is unnecessary.

AI Collection is included as a maintainer-affiliated paid candidate with the same fit and authorization rules. Display the affiliation in the shortlist and paid recommendation report. A catalog price is an observation, never a checkout guarantee. Use the current official submission/checkout to resolve contradictory prices or free-review claims before execution.

Existing listings must be checked before submitting. Identify a product using its canonical homepage and identity, not just its name. Namesakes require operator review. Do not overwrite another product or create a duplicate merely to satisfy a campaign count.

## 6. Status and evidence rules

Keep campaign fulfillment, individual listing state, public-page availability, payment state, and handoff state separate.

Campaign lifecycle: `draft`, `awaiting_service_payment`, `researching`, `awaiting_customer_approval`, `in_progress`, `delivered`, `closed`, `cancelled`. Payment failure/unknown is a billing state, not proof of a completed campaign. A delivered report may still contain pending editorial reviews or future launches.

Listing states:

| State | Required meaning |
| --- | --- |
| candidate | Discovered; not selected or prepared. |
| prepared | Selected fields ready; no successful submission established. |
| submitted | Receipt establishes submission; further publication state unknown. |
| pending_review | Destination explicitly says editorial review is pending. |
| scheduled | Destination confirms a future launch date. |
| live | Correct public listing observed and verified; record URL, verifier, and time. |
| needs_user | A specific open customer task prevents progress. |
| blocked | A technical/account/eligibility issue prevents progress without a current customer task. |
| rejected | Destination explicitly rejects the listing. |
| skipped | Deliberately not attempted; record reason. |

Transitions are guarded by evidence rather than a rigid linear sequence. A verified listing can return to review, be rejected, or become unavailable; preserve history. Task resolution returns the entry to its last established state, not automatically to live. Imported or customer-reported “live” is a claim awaiting verification until the app records an observed public page. Provide an operator correction flow with a reason; never overwrite audit history.

Store public-page availability and verified timestamp separately. Count every destination once by its current listing state, even when both a public profile and scheduled launch exist. Show prepared/rejected/skipped/blocked rows when present; totals must reconcile with the campaign's selected entries.

Evidence kinds: observed public page, destination receipt, schedule confirmation, payment confirmation, owner report, operator note. Store source, timestamp, actor, optional safe URL and private attachment. An operator attestation can document a manual check; it must say what was observed. Evidence is private by default. Receipts and management pages are not public listing URLs, and guessed slugs are never verified results.

## 7. Authorization, accounts, and costs

Customer approval authorizes the selected project-profile revision, destination list, and scoped work. Added destinations, material copy/URL changes, new required backlinks, a new plan/cadence, or spend beyond an approved ceiling need updated approval. Preserve already completed entries. An ordinary retry of an unchanged authorized action does not demand a new campaign approval, but tool-required action-time confirmations still apply.

Terms/privacy agreement, CAPTCHA, login, credential creation, and payment prompts must follow the execution tool/site requirements. A dashboard approval cannot bypass a required action-time confirmation. Human-only communities stay human-authored and human-submitted. For those sites, do not generate the post title/body for the customer to paste.

MVP account model: customer-owned directory accounts. Operator handles public/non-authenticated steps when authorized; customer handles authenticated work in their own browser if no approved delegation exists. Do not create operator-owned listings that the customer cannot manage. Show ownership/management follow-up explicitly.

MVP monetary rules:

- Service fee is one-time USD checkout on the website. Directory spending is a separate USD budget/ledger. Store integer minor units; null means unknown, never zero.
- Only USD directory purchases are supported initially. Other currencies can be researched but require a manual blocked/needs-user outcome; no implicit conversion.
- Customer pays each directory on its own website. Never collect directory money or card details in this app.
- Paid authorization identifies destination, plan, purpose, currency, ceiling, one-time cadence, and source/timestamp. A total budget alone does not select a plan. Recurring directory plans are research-only in MVP.
- Reserve approved purchases atomically against the directory budget. A purchase's confirmed charge replaces its reservation; do not count both. Prevent approvals whose active reservations plus confirmed spend exceed the budget.
- An ambiguous payment retains its reservation and displays Unknown. Check the receipt/order before retrying. A customer “I paid” update is recorded as reported, not independently confirmed.
- Refunds and reservation releases are explicit ledger events with references/reasons. Release uncertain reservations only after reconciliation. Directory and service refunds are separate.

The app enforces its own approval/budget state and records external actions; it cannot enforce what a human does in an unrelated browser. Do not market audit records as a guarantee that all external actions were technically prevented.

## 8. Data model

Use a relational database with tenant-scoped foreign keys and server-side authorization on every read/write/export. Suggested entities:

| Entity | Core fields / relationships |
| --- | --- |
| User / Workspace / Membership | Auth subject, workspace owner, role; MVP one customer owner per workspace. |
| OperatorAssignment | Operator, campaign, assigned/revoked times; catalog admin permission separate from campaign access. |
| Project / ProfileRevision | Workspace, canonical homepage, original URL, facts, source/provenance, descriptions, contact, approved revision, timestamps. |
| Asset | Workspace/project, private object key, MIME/size, owner approval, safe upload filename. |
| Directory / DirectoryPlanObservation | Official URLs, fit tags, eligibility, conditions, affiliation, observed price/currency/cadence, check timestamp/source. |
| Offer / OfferSnapshot | Service scope, attempt limit, test/live price reference, terms version; immutable purchased campaign copy. |
| Campaign | Workspace/project, offer snapshot, mode (`research_only`, `prepare`, `submit`), lifecycle, customer timezone, directory budget, assigned operator, timestamps. |
| CampaignEntry | Campaign/directory, selected profile revision, fit/cost/conditions snapshot, state, submitted homepage/repository, observed public/receipt/management URLs, launch date/timezone, verification fields. |
| Approval | Campaign/entry, exact approved revision/scope/plan/ceiling, actor/time, superseded/revoked state. |
| SubmissionAttempt | Entry, intent/idempotency key, operator, attempt state, started/completed times, observed result; unknown remains unresolved. |
| HandoffTask | Entry, customer action/reason/safe URL, open/reported_done/verified/declined, actor/timestamps, non-secret notes. |
| Evidence / EntryEvent | Entry/attempt, evidence kind/source/verification level, private object key or safe URL; append-only status/action history. |
| ServiceOrder / PaymentEvent | Campaign, provider checkout/payment IDs, expected amount/currency/offer, confirmed state, unique provider event ID. |
| DirectorySpendEvent | Entry, authorization, reservation/charge/refund/release, amount/currency, payment certainty and reference; append-only. |
| ReportSnapshot | Campaign, generation time, report version, public-safe projection, private export references. |

Normalize homepage identity for duplicate checks without deleting meaningful paths or conflating all products on the same host. Preserve the submitted original URL. Unique campaign/directory selection prevents accidental duplicate entries; history supports legitimate later updates/relaunches.

Support importing/exporting [campaign-template.json](../assets/campaign-template.json) schema version 1. Validate uploaded files and show an import preview. Treat `entry_template` as a template, not a row. Preserve source history and claimed state; require verification before claiming live/confirmed payment. Imported approvals are historical references, not new execution authorization. New spend approval is required inside the app. Handle missing legacy fields as unknown; never infer confirmed purchases from a price.

## 9. Architecture and implementation defaults

Build a separate web application. Recommended starting shape: TypeScript application, a maintained full-stack web framework, PostgreSQL with migrations, managed authentication, private object storage, and hosted one-time checkout. The builder should select currently supported versions and document choices; no specific library release is mandated by this spec.

Keep MVP deployment small: one web service and database/storage integrations. No browser execution infrastructure or distributed agent fleet. Catalog research, submission, and verification can be operator actions. Any asynchronous import/export work should have durable job state and bounded retries; do not require Redis or a separate workflow engine without a demonstrated need.

Server modules: identity/access; project revisions/assets; catalog; campaign/approval/task state; evidence/reporting; service billing; third-party spend accounting. Expose explicit service boundaries so a future authenticated MCP client can call the same permission-checked operations.

Service billing uses server-created checkout sessions and signed, idempotent webhook processing. Verify order/workspace, expected offer, amount and currency; browser redirects cannot alter payment state. Duplicate or out-of-order events cannot trigger duplicate fulfillment or duplicate charges. If payment is received after cancellation, record it and flag reconciliation; do not silently restart work. Production charges/emails/deployment are outside the initial build authorization.

Enforce campaign mode on mutation routes: research-only cannot create submission attempts or spend authorizations; prepare mode can assemble fields but cannot execute submission work. Moving to submit mode requires the customer's scope approval. Mode is independent of whether a service order exists, so purchasing research does not authorize publication.

No automatic remote fetching is required for MVP: a supplied homepage is a link and fact source for the operator. If the builder adds website metadata extraction, enforce HTTP(S)-only URLs, DNS/IP restrictions against private/link-local/loopback targets, redirect revalidation, bounded size/time, and no authenticated browsing. Treat fetched content as untrusted data; extracted facts need customer review. Do not fetch arbitrary report URLs server-side just to render the table.

Manual local operation and mocked external integrations must work without production credentials. Missing integration configuration should show a setup state, never a fake successful payment or submission. Do not reuse, read, or copy secrets from any Antaeus workspace `.env`.

## 10. Security, privacy, and operations

- All customer data, evidence, billing state, and reports require authentication and tenant checks. Operator access is assigned and audited. Unassigned operators and catalog-only admins cannot read campaign data.
- Uploads have allowed formats, size limits, content inspection, private storage, authorization-checked downloads and short-lived access URLs. Escape/sanitize user text and report exports; reject executable uploads. Do not render arbitrary HTML from scraped pages or evidence.
- Customer screenshots may contain secrets. Explain upload visibility, provide deletion/replacement, and require a share-safe check before evidence is included in an exported report. Do not promise automated secret redaction.
- Do not log credentials, raw payment payloads, customer email bodies, or token-bearing URLs. Safe URL validation applies to stored action links and exports. Never use user-provided strings as executable shell commands.
- Use atomic state changes and optimistic concurrency for approvals, reservations, task resolution and status edits. Keep one active submission intent per entry. A restarted operator session sees unresolved attempts before starting another.
- Audit events include actor/time and the relevant revision/action; preserve corrections as new events. Customer deletion requests must include a defined purge process; billing/audit retention follows the owner's published policy. Do not invent a legal retention period.
- In-app task notifications are sufficient for MVP. Transactional email is optional/configured and must be test/sandbox-only during the build. No broad mailing list, outreach, or marketing enrollment.

## 11. Final report contract

Deliver an authenticated web report and downloadable Markdown, CSV, and JSON. Use the existing [report template](../assets/report-template.md) and [fictional example](../references/example-report.md) as semantic references, not literal placeholder UI.

The report contains:

1. Project name/homepage, generated timestamp, and counts by distinct current status.
2. Separate service fee and directory-spend summaries: confirmed charges, unresolved payments, active reservations, budget remaining, and refunds. No combined misleading “total” across unconfirmed values.
3. One row per destination: name, verified public link or clearly labelled safe receipt/form link, actual status, charge/certainty, launch date/timezone, next action, last verification time.
4. A customer action list with site-specific instructions and safe destination links.
5. Skipped/rejected/blocked reasons and paid candidates awaiting selection, clearly separate from completed purchases.
6. AI Collection affiliation whenever it is recommended or included.

Downloads default to a share-safe projection that excludes contacts, account identifiers, management links, private receipts, internal notes, and attachments. Replace private receipts with “Receipt recorded privately.” The owner may explicitly export the private ledger separately with a clear scope label. Sanitize CSV cells against spreadsheet formula injection. No public share links in MVP.

## 12. Acceptance criteria

These are meaningful integration/behavior checks, not tests of exact copy.

| Scenario | Required result |
| --- | --- |
| New campaign | Directory spend is zero; no destinations or plans implicitly approved. |
| Research-only work | Can prepare a shortlist/report; no submission intent or purchase authorization created. |
| Free-only + required badge | Row is conditional-free and held/skipped; no website edits or paid fallback. |
| Homepage + repository | Submission fields use approved homepage; repository remains supplementary. |
| Existing namesake | Operator must resolve identity; no automatic overwrite or duplicate submission. |
| Edited product facts | Changed revision requires new approval for unexecuted affected rows; completed history remains intact. |
| Receipt upload | Establishes receipt/review state, never automatically live. |
| Public profile + future launch | Public link is available while current row remains scheduled; counts once. |
| Customer reports completion | Creates reported result awaiting verification; cannot directly confirm public status or payment. |
| Two concurrent spend approvals | Atomic reservations prevent exceeding the approved directory budget. |
| Unknown directory payment | Reservation remains; no fresh payment attempt until reconciled. |
| Confirmed charge | Replaces its own reservation without double-counting spend. |
| Recurring or non-USD directory plan | Research/handoff only; no supported purchase approval. |
| Duplicate/out-of-order service webhook | Exactly one order/fulfillment transition; no duplicate charge or campaign. |
| Cancelled campaign then late payment | Records payment and flags reconciliation; does not restart execution. |
| Login/password/CAPTCHA/human-only step | Creates specific user task; no secrets collected or prohibited generated post supplied. |
| Cross-tenant or unassigned operator | Server denies records, evidence, exports and mutations, including direct object IDs. |
| Import legacy ledger | Previewed, version-validated, no template row import, unknown values preserved; no inherited execution authority. |
| Restart after ambiguous submission | Existing unresolved attempt is visible; duplicate intent is blocked pending reconciliation. |
| Report export | Counts reconcile; link types explicit; private fields omitted; CSV formulas neutralized. |
| AI Collection recommendation | Fit reason and affiliation visible; no automatic selection or purchase. |
| No production integrations | Local/sandbox workflow works and clearly labels mock states; no fake real-world success. |

Also verify responsive customer/operator screens, keyboard navigation, labelled forms, readable statuses that do not depend only on color, empty/loading/error states, and database migrations against a clean database.

## 13. Build order and definition of done

1. Create the separate application repo, document stack decisions, build schema/access control, seed directories and fictional fixtures.
2. Deliver project/profile revisions, campaign setup, catalog/shortlist approval and private dashboard.
3. Add operator assignments, evidence/history, guarded status changes, tasks and report exports.
4. Add test-mode service checkout/webhooks and the separate directory authorization/reservation ledger.
5. Validate acceptance scenarios and the full customer/operator journey with fixtures; provide setup/run/test instructions and a demo walkthrough.

MVP done means a fresh local environment can complete one fictional free campaign and one fictional mixed campaign end to end, including a payment uncertainty case and a customer handoff, with truthful exports. No live directory submissions, real charges, real emails, public deployment, or marketplace publication are required to demonstrate completion.

## 14. Later releases and launch decisions

After paid pilot customers validate the operational workflow, consider opt-in publication checks, maintained directory health/pricing data, agency workspaces, narrowly scoped browser adapters, and a plugin/MCP integration. Credentials and human confirmations remain user-controlled.

For public plugin distribution, recheck platform policies at implementation/submission time. On October 15, 2026, [OpenAI plugin commerce rules](https://developers.openai.com/plugins/plugin-guidelines#commerce-and-monetization) allowed access to an existing paid account but restricted digital-service checkout/upsells. Keep purchase flows on the website; do not assume a public plugin may initiate paid directory checkout. Claude supports [plugin distribution](https://code.claude.com/docs/en/plugins/publish), while its [commercial partner marketplace](https://claude.com/marketplace-partners) is a separate application route. Neither is required for this MVP.

Owner decisions before production: final name/domain, service price and attempt limit, operational capacity/turnaround, refund/cancellation/retention policies, final integration/hosting choices, legal pages, real payment/email configuration, and explicit launch authorization. Record assumptions now and build with fixtures; do not silently make these commercial commitments.
