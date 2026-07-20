# Leap: Native API Reference

A consolidated summary of Leap's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.api.jobprogress.com/
- **API base URL:** `https://api.jobprogress.com/api/v3`

## Authentication

### Access Token

Provider-generated Leap access token pasted as a secret and sent as a Bearer token on every request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.api.jobprogress.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Job Note](actions/add-job-note.md) | `POST /jobs/[:jobId]/notes` | [docs](https://docs.api.jobprogress.com/api/job-note.json) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://docs.api.jobprogress.com/api/customer.json) |
| [Create Job](actions/create-job.md) | `POST /jobs` | [docs](https://docs.api.jobprogress.com/api/job.json) |
| [Get Customer](actions/get-customer.md) | `GET /customers/[:customerId]` | [docs](https://docs.api.jobprogress.com/api/customer.json) |
| [Get Job](actions/get-job.md) | `GET /jobs/[:jobId]` | [docs](https://docs.api.jobprogress.com/api/job.json) |
| [List Categories](actions/list-categories.md) | `GET /item_categories` | [docs](https://docs.api.jobprogress.com/#/GET-item_categories) |
| [List Company Trades](actions/list-company-trades.md) | `GET /company/trades` | [docs](https://docs.api.jobprogress.com/) |
| [List Countries](actions/list-countries.md) | `GET /countries` | [docs](https://docs.api.jobprogress.com/#/GET-countries) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://docs.api.jobprogress.com/api/customer.json) |
| [List Divisions](actions/list-divisions.md) | `GET /divisions` | [docs](https://docs.api.jobprogress.com/#/GET-divisions) |
| [List Job Notes](actions/list-job-notes.md) | `GET /jobs/[:jobId]/notes` | [docs](https://docs.api.jobprogress.com/api/job-note.json) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://docs.api.jobprogress.com/api/job.json) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /company/payment_types` | [docs](https://docs.api.jobprogress.com/#/GET-company-payment_types) |
| [List States](actions/list-states.md) | `GET /countries/[:countryId]/states` | [docs](https://docs.api.jobprogress.com/#/GET-countries-countryId-states) |
| [List Suppliers](actions/list-suppliers.md) | `GET /suppliers` | [docs](https://docs.api.jobprogress.com/#/GET-suppliers) |
| [List Users](actions/list-users.md) | `GET /company/users` | [docs](https://docs.api.jobprogress.com/#/GET-company-users) |
| [List Workflow Stages](actions/list-workflow-stages.md) | `GET /workflow/stages` | [docs](https://docs.api.jobprogress.com/#/GET-workflow-stages) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/[:customerId]` | [docs](https://docs.api.jobprogress.com/api/customer.json) |
| [Update Job](actions/update-job.md) | `PUT /jobs/[:jobId]` | [docs](https://docs.api.jobprogress.com/api/job.json) |
| [Update Job Note](actions/update-job-note.md) | `PUT /jobs/notes/[:noteId]` | [docs](https://docs.api.jobprogress.com/api/job-note.json) |
