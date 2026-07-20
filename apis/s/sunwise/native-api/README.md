# Sunwise: Native API Reference

A consolidated summary of Sunwise's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://production.sunwise.ai/boty/docs
- **OpenAPI specification:** https://production.sunwise.ai/boty/api/v1/openapi.json
- **API base URL:** `https://production.sunwise.ai/boty/api/v1`

## Authentication

### Sunwise Login

OAuth2 password-grant login using the Sunwise account email and password.

### Credentials

- **Username:** `username` · required · Sunwise account email
- **Password:** `password` · required · Sunwise account password

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://production.sunwise.ai/boty/api/v1/login/access-token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://academy.sunwise.mx/es/articles/12054073-sunwise-api)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Create Projects No Files](actions/bulk-create-projects-no-files.md) | `POST /projects/bulk-create-no-files` | [docs](https://production.sunwise.ai/boty/docs) |
| [Bulk Create Projects With Files](actions/bulk-create-projects-with-files.md) | `POST /projects/bulk-create` | [docs](https://production.sunwise.ai/boty/docs) |
| [Contact Projects](actions/contact-projects.md) | `GET /projects/contact-projects/:contact_id/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Create Contact](actions/create-contact.md) | `POST /contacts/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Create Project Without Consumption](actions/create-project-without-consumption.md) | `POST /projects/create-project-without-consumption/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Create Proposal In Project](actions/create-proposal-in-project.md) | `POST /proposals/:project_id/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Create Report](actions/create-report.md) | `POST /reports/create-report` | [docs](https://production.sunwise.ai/boty/docs) |
| [Download Proposals Csv](actions/download-proposals-csv.md) | `GET /proposals/csv/:proposal_id` | [docs](https://production.sunwise.ai/boty/docs) |
| [Download Report Csv](actions/download-report-csv.md) | `GET /reports/csv/:report_id/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Get Active Report](actions/get-active-report.md) | `GET /reports/active-report/:report_id/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Get Active Reports](actions/get-active-reports.md) | `GET /reports/active-reports/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Get Favorite Commercial Offer](actions/get-favorite-commercial-offer.md) | `GET /projects/favorite-commercial-offer/:project_id` | [docs](https://production.sunwise.ai/boty/docs) |
| [Get Project](actions/get-project.md) | `GET /projects/:project_id/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Get Proposal](actions/get-proposal.md) | `GET /proposals/:proposal_id/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Group Files](actions/group-files.md) | `POST /projects/group-files` | [docs](https://production.sunwise.ai/boty/docs) |
| [Health](actions/health.md) | `GET /health` | [docs](https://production.sunwise.ai/boty/docs) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Project Search](actions/project-search.md) | `GET /projects/project-search/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Proposal Search](actions/proposal-search.md) | `GET /proposals/proposal-search/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Recent Projects](actions/recent-projects.md) | `GET /projects/recent-projects/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Search Contacts](actions/search-contacts.md) | `GET /contacts-search/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Search Reports](actions/search-reports.md) | `GET /reports/report-search/` | [docs](https://production.sunwise.ai/boty/docs) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contact_id/` | [docs](https://production.sunwise.ai/boty/docs) |
