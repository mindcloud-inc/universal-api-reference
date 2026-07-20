# OneSuite: Native API Reference

A consolidated summary of OneSuite's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://rest-api.onesuite.io/
- **API base URL:** `https://api.onesuite.io`

## Authentication

### API Key

Use a personal OneSuite API key generated from Settings > API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://rest-api.onesuite.io/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `opportunityStages`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Connect Opportunity to Company](actions/connect-opportunity-to-company.md) | `POST /v1/opportunities/:opportunity_id/company` | [docs](https://rest-api.onesuite.io/#connect-opportunity-company) |
| [Connect Person to Company](actions/connect-person-to-company.md) | `POST /v1/people/:people_id/company` | [docs](https://rest-api.onesuite.io/#connect-people-to-company) |
| [Connect Person to Opportunity](actions/connect-person-to-opportunity.md) | `POST /v1/people/:people_id/opportunity` | [docs](https://rest-api.onesuite.io/#connect-people-to-opportunity) |
| [Convert Company to Client](actions/convert-company-to-client.md) | `POST /v1/companies/:company_id/convert-to-client` | [docs](https://rest-api.onesuite.io/#convert-company-to-client) |
| [Convert Opportunity to Client](actions/convert-opportunity-to-client.md) | `POST /v1/opportunities/:opportunity_id/convert-to-client` | [docs](https://rest-api.onesuite.io/#convert-opportunity-to-client) |
| [Create Client](actions/create-client.md) | `POST /v2/clients` | [docs](https://rest-api.onesuite.io/#create-client-with-all-fields) |
| [Create Client Project](actions/create-client-project.md) | `POST /v1/clients/:client_id/projects` | [docs](https://rest-api.onesuite.io/#create-client-project) |
| [Create Company](actions/create-company.md) | `POST /v2/companies` | [docs](https://rest-api.onesuite.io/#create-company-with-all-fields) |
| [Create Invoice](actions/create-invoice.md) | `POST /v1/invoices` | [docs](https://rest-api.onesuite.io/#create-invoice) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /v2/opportunities` | [docs](https://rest-api.onesuite.io/#create-opportunity-with-all-fields) |
| [Create Person](actions/create-person.md) | `POST /v2/people` | [docs](https://rest-api.onesuite.io/#create-people-with-all-fields) |
| [Create Project](actions/create-project.md) | `POST /v1/projects` | [docs](https://rest-api.onesuite.io/#create-project) |
| [Get Client](actions/get-client.md) | `GET /v1/clients/:client_id` | [docs](https://rest-api.onesuite.io/#get-specific-client) |
| [Get Company](actions/get-company.md) | `GET /v1/companies/:company_id` | [docs](https://rest-api.onesuite.io/#get-single-company) |
| [Get Invoice](actions/get-invoice.md) | `GET /v1/invoices/:invoice_id` | [docs](https://rest-api.onesuite.io/#get-specific-invoice) |
| [Get Opportunity](actions/get-opportunity.md) | `GET /v1/opportunities/:opportunity_id` | [docs](https://rest-api.onesuite.io/#get-single-opportunity) |
| [Get Opportunity Stages](actions/get-opportunity-stages.md) | `GET /v1/opportunities/stage` | [docs](https://rest-api.onesuite.io/) |
| [Get Person](actions/get-person.md) | `GET /v1/people/:people_id` | [docs](https://rest-api.onesuite.io/#get-single-people) |
| [Get Project](actions/get-project.md) | `GET /v1/projects/:project_id` | [docs](https://rest-api.onesuite.io/#get-specific-project) |
| [List Client Invoices](actions/list-client-invoices.md) | `GET /v1/clients/:client_id/invoices` | [docs](https://rest-api.onesuite.io/#get-client-invoices) |
| [List Client Projects](actions/list-client-projects.md) | `GET /v1/clients/:client_id/projects` | [docs](https://rest-api.onesuite.io/#get-client-projects) |
| [List Clients](actions/list-clients.md) | `GET /v1/clients` | [docs](https://rest-api.onesuite.io/#get-all-clients) |
| [List Companies](actions/list-companies.md) | `GET /v1/companies` | [docs](https://rest-api.onesuite.io/#get-all-companies) |
| [List Company People](actions/list-company-people.md) | `GET /v1/companies/:company_id/people` | [docs](https://rest-api.onesuite.io/#get-company-people) |
| [List Invoices](actions/list-invoices.md) | `GET /v1/invoices` | [docs](https://rest-api.onesuite.io/#get-all-invoices) |
| [List Opportunities](actions/list-opportunities.md) | `GET /v1/opportunities` | [docs](https://rest-api.onesuite.io/#get-all-opportunities) |
| [List People](actions/list-people.md) | `GET /v1/people` | [docs](https://rest-api.onesuite.io/#get-all-people) |
| [List Project Sections](actions/list-project-sections.md) | `GET /v1/projects/:project_id/sections` | [docs](https://rest-api.onesuite.io/#get-all-sections) |
| [List Projects](actions/list-projects.md) | `GET /v1/projects` | [docs](https://rest-api.onesuite.io/#get-all-projects) |
| [List Section Tasks](actions/list-section-tasks.md) | `GET /v1/projects/:project_id/sections/:section_id/tasks` | [docs](https://rest-api.onesuite.io/#get-all-tasks-of-section) |
| [Update Client](actions/update-client.md) | `PATCH /v2/clients/:client_id` | [docs](https://rest-api.onesuite.io/#update-client-with-all-fields) |
| [Update Client Priority](actions/update-client-priority.md) | `PATCH /v1/clients/:client_id/priority` | [docs](https://rest-api.onesuite.io/#update-client-39-s-priority-assignment) |
| [Update Client Status](actions/update-client-status.md) | `PATCH /v1/clients/:client_id/status` | [docs](https://rest-api.onesuite.io/#update-client-39-s-status-assignment) |
| [Update Company](actions/update-company.md) | `PATCH /v2/companies/:company_id` | [docs](https://rest-api.onesuite.io/#update-company) |
| [Update Invoice](actions/update-invoice.md) | `PATCH /v1/invoices/:invoice_id` | [docs](https://rest-api.onesuite.io/#edit-invoice) |
| [Update Invoice Status](actions/update-invoice-status.md) | `PATCH /v1/invoices/:invoice_id/payment-status` | [docs](https://rest-api.onesuite.io/#change-invoice-status) |
| [Update Opportunity](actions/update-opportunity.md) | `PATCH /v2/opportunities/:opportunity_id` | [docs](https://rest-api.onesuite.io/#update-opportunity) |
| [Update Opportunity Stage](actions/update-opportunity-stage.md) | `PATCH /v1/opportunities/:opportunity_id/stage` | [docs](https://rest-api.onesuite.io/#update-opportunity-stage) |
| [Update Person](actions/update-person.md) | `PATCH /v2/people/:people_id` | [docs](https://rest-api.onesuite.io/#update-people) |
| [Update Project](actions/update-project.md) | `PATCH /v1/projects/:project_id` | [docs](https://rest-api.onesuite.io/#edit-project) |
