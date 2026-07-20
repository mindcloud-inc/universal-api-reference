# Streamtime: Native API Reference

A consolidated summary of Streamtime's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.streamtime.net/v2/swagger
- **OpenAPI specification:** https://api.streamtime.net/v2/swagger.json
- **API base URL:** `https://api.streamtime.net/v2`

## Authentication

### API Key

Authenticate with your Streamtime API key. Streamtime expects the key in the Authorization header as Bearer <key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.streamtime.net/en/articles/12854233-using-the-streamtime-public-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://api.streamtime.net/v2/swagger#/Companies/createCompany) |
| [Create Company Contact](actions/create-company-contact.md) | `POST /companies/:company_id/contacts` | [docs](https://api.streamtime.net/v2/swagger#/Companies/createCompanyContact) |
| [Create Job](actions/create-job.md) | `POST /jobs` | [docs](https://api.streamtime.net/v2/swagger#/Jobs/createJob) |
| [Create Job Item](actions/create-job-item.md) | `POST /jobs/:job_id/job_items` | [docs](https://api.streamtime.net/v2/swagger#/Jobs/createJobItem) |
| [Create Job Phase](actions/create-job-phase.md) | `POST /jobs/:job_id/job_phases` | [docs](https://api.streamtime.net/v2/swagger#/Jobs/createJobPhase) |
| [Create Logged Time Entry](actions/create-logged-time-entry.md) | `POST /logged_times` | [docs](https://api.streamtime.net/v2/swagger#/ToDos/createLoggedTime) |
| [Create Multiple Logged Time Entries](actions/create-multiple-logged-time-entries.md) | `POST /logged_times/bulk` | [docs](https://api.streamtime.net/v2/swagger#/ToDos/createLoggedTimeBulk) |
| [Get Company](actions/get-company.md) | `GET /companies/:company_id` | [docs](https://api.streamtime.net/v2/swagger#/Companies/getCompany) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:invoice_id` | [docs](https://api.streamtime.net/v2/swagger#/Invoices/getInvoice) |
| [Get Job](actions/get-job.md) | `GET /jobs/:job_id` | [docs](https://api.streamtime.net/v2/swagger#/Jobs/getJob) |
| [Get Logged Time Entry](actions/get-logged-time-entry.md) | `GET /logged_times/:logged_time_id` | [docs](https://api.streamtime.net/v2/swagger#/ToDos/getLoggedTime) |
| [Get Organisation](actions/get-organisation.md) | `GET /organisation` | [docs](https://api.streamtime.net/v2/swagger#/Organisation/getOrganisation) |
| [Get Quote](actions/get-quote.md) | `GET /quotes/:quote_id` | [docs](https://api.streamtime.net/v2/swagger#/Quotes/getQuote) |
| [Get User](actions/get-user.md) | `GET /users/:user_id` | [docs](https://api.streamtime.net/v2/swagger#/Users/getUser) |
| [List Company Contacts](actions/list-company-contacts.md) | `GET /companies/:company_id/contacts` | [docs](https://api.streamtime.net/v2/swagger#/Companies/listCompanyContacts) |
| [List Invoice Line Items](actions/list-invoice-line-items.md) | `GET /invoices/:invoice_id/invoice_line_items` | [docs](https://api.streamtime.net/v2/swagger#/Invoices/getInvoiceLineItems) |
| [List Job Items](actions/list-job-items.md) | `GET /jobs/:job_id/job_items` | [docs](https://api.streamtime.net/v2/swagger#/Jobs/listJobItems) |
| [List Job Phases](actions/list-job-phases.md) | `GET /jobs/:job_id/job_phases` | [docs](https://api.streamtime.net/v2/swagger#/Jobs/listJobPhases) |
| [List Quote Line Items](actions/list-quote-line-items.md) | `GET /quotes/:quote_id/quote_line_items` | [docs](https://api.streamtime.net/v2/swagger#/Quotes/listQuoteLineItems) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://api.streamtime.net/v2/swagger#/Users/listUsers) |
| [Search Records](actions/search-records.md) | `POST /search` | [docs](https://api.streamtime.net/v2/swagger#/Search/searchRecords) |
| [Update Job](actions/update-job.md) | `PUT /jobs/:job_id` | [docs](https://api.streamtime.net/v2/swagger#/Jobs/updateJob) |
| [Update Job Status](actions/update-job-status.md) | `PUT /jobs/:job_id/job_status` | [docs](https://api.streamtime.net/v2/swagger#/Jobs/updateJobStatus) |
| [Update Logged Time Entry](actions/update-logged-time-entry.md) | `PUT /logged_times/:logged_time_id` | [docs](https://api.streamtime.net/v2/swagger#/ToDos/updateLoggedTime) |
