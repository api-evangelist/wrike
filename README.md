# Wrike (wrike)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Wrike is a collaborative work management platform used by 30,000+ organizations. The Wrike Developer Platform exposes a REST API v4 for building integrations and automations against tasks, folders, projects, contacts, workflows, time tracking, custom fields, audit logs, and webhooks. The platform also offers the DataHub Public API for raw analytical data, a BI Export API for piping data into Tableau, Power BI, or Looker, a Cloud Content Connector for managing cloud-based content assets, and a Wrike MCP Server for connecting Wrike to AI assistants such as Claude, ChatGPT, and Microsoft Copilot Studio. Authentication is handled via OAuth 2.0 or permanent access tokens.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/wrike/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/wrike/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Work Management
- Project Management
- Collaboration
- Productivity
- Workflow Automation
- Task Management

## Timestamps

- **Created:** 2025-01-08
- **Modified:** 2026-05-19

## APIs

### Wrike API

The Wrike REST API v4 enables developers to build integrations and automations for Wrike. The API provides programmatic access to tasks, folders, projects, contacts, workflows, time tracking, timesheets, custom fields, audit logs, webhooks, and more. Authentication uses OAuth 2.0 or permanent access tokens, and the base URL is https://www.wrike.com/api/v4.

- **Human URL:** [https://developers.wrike.com/api/v4/](https://developers.wrike.com/api/v4/)
- **Base URL:** `https://www.wrike.com/api/v4`

#### Tags

- REST API
- Work Management
- Project Management
- Tasks
- Workflows
- Webhooks

#### Properties

- [Documentation](https://developers.wrike.com/)
- [API Reference](https://developers.wrike.com/api/v4/)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/wrike/refs/heads/main/openapi/wrike-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Authentication](https://developers.wrike.com/oauth-2-0-authorization)
- [Getting Started](https://developers.wrike.com/getting-started/)
- [Changelog](https://developers.wrike.com/changelog/)
- [Postman Collection](collections/wrike.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wrike.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Wrike DataHub Public API

The Wrike DataHub Public API provides programmatic access to raw analytical data from Wrike, enabling custom reporting and integration with downstream analytics platforms.

- **Human URL:** [https://developers.wrike.com/datahub-public-api/](https://developers.wrike.com/datahub-public-api/)

#### Tags

- Analytics
- Reporting
- DataHub

#### Properties

- [Documentation](https://developers.wrike.com/datahub-public-api/)
- [Postman Collection](collections/wrike.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wrike.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Wrike BI Export API

The Wrike BI Export API lets you export Wrike data into business intelligence tools such as Tableau, Power BI, and Looker for enterprise-grade reporting and analysis.

- **Human URL:** [https://developers.wrike.com/bi-export-api/](https://developers.wrike.com/bi-export-api/)

#### Tags

- Business Intelligence
- Export
- Analytics

#### Properties

- [Documentation](https://developers.wrike.com/bi-export-api/)
- [Postman Collection](collections/wrike.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wrike.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Wrike Cloud Content Connector

The Wrike Cloud Content Connector enables management of cloud-based content assets within Wrike workflows, integrating external content providers with Wrike tasks and projects.

- **Human URL:** [https://developers.wrike.com/cloud-content-connector/](https://developers.wrike.com/cloud-content-connector/)

#### Tags

- Content Management
- Cloud Storage
- Connector

#### Properties

- [Documentation](https://developers.wrike.com/cloud-content-connector/)
- [Postman Collection](collections/wrike.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wrike.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Wrike MCP Server

The Wrike MCP Server connects Wrike directly to AI assistants such as Claude, ChatGPT, and Microsoft Copilot Studio using the Model Context Protocol, enabling AI-driven workflows over Wrike data.

- **Human URL:** [https://developers.wrike.com/mcp-server/](https://developers.wrike.com/mcp-server/)

#### Tags

- MCP
- AI
- Model Context Protocol

#### Properties

- [Documentation](https://developers.wrike.com/mcp-server/)
- [Postman Collection](collections/wrike.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wrike.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/wrike)
- [Developer Portal](https://developers.wrike.com/)
- [Sign Up](https://www.wrike.com/free-trial/)
- [Pricing](https://www.wrike.com/price/)
- [Terms of Service](https://www.wrike.com/developer-terms/)
- [Privacy Policy](https://www.wrike.com/security/privacy/)
- [Status Page](https://status.wrike.com/)
- [Support](https://help.wrike.com/hc/en-us/)
- [F A Q](https://developers.wrike.com/faq/)
- [Blog](https://www.wrike.com/blog/)
- [Webinars](https://www.wrike.com/webinars/)
- [Training](https://www.wrike.com/discover/)
- [Professional Services](https://www.wrike.com/professional-services/)
- [GitHub Organization](https://github.com/wrike)
- [Changelog](https://developers.wrike.com/changelog/)
- [Compliance](https://www.wrike.com/security/)
- [Features](undefined)
- [Use Cases](undefined)
- [Solutions](undefined)
- [Integrations](undefined)
- [M C P Server](https://github.com/wrike/datahub-mcp)
- [L L Ms Txt](https://developers.wrike.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
