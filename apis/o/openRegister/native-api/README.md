# OpenRegister: Native API Reference

A consolidated summary of OpenRegister's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://docs.openregister.de
- **API base URL:** `https://api.openregister.de`

## Authentication

### API Key

Authenticate to OpenRegister with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.openregister.de/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `results`. The total page count is read from `pagination.total_pages`. The current page number is read from `pagination.page`.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–30). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Advanced Company Search](actions/advanced-company-search.md) | `POST /v1/search/company` | [docs](https://docs.openregister.de/endpoint/filter-company) |
| [Autocomplete Companies](actions/autocomplete-companies.md) | `GET /v1/autocomplete/company` | [docs](https://docs.openregister.de/endpoint/autocomplete-company) |
| [Get Company](actions/get-company.md) | `GET /v1/company/:company_id` | [docs](https://docs.openregister.de/endpoint/company) |
| [Get Company Contact Information](actions/get-company-contact-information.md) | `GET /v0/company/:company_id/contact` | [docs](https://docs.openregister.de/endpoint/company-contact) |
| [Get Company Historical Owners](actions/get-company-historical-owners.md) | `GET /v1/company/:company_id/owners/historical` | [docs](https://docs.openregister.de/endpoint/company-historical-owners) |
| [Get Company Holdings](actions/get-company-holdings.md) | `GET /v1/company/:company_id/holdings` | [docs](https://docs.openregister.de/endpoint/company-holdings) |
| [Get Company Owners](actions/get-company-owners.md) | `GET /v1/company/:company_id/owners` | [docs](https://docs.openregister.de/endpoint/company-owners) |
| [Get Company UBOs](actions/get-company-ubos.md) | `GET /v1/company/:company_id/ubo` | [docs](https://docs.openregister.de/endpoint/company-ubo) |
| [Get Person](actions/get-person.md) | `GET /v1/person/:person_id` | [docs](https://docs.openregister.de/endpoint/person) |
| [Get Person Holdings](actions/get-person-holdings.md) | `GET /v1/person/:person_id/holdings` | [docs](https://docs.openregister.de/endpoint/person-holdings) |
| [Get Realtime Document](actions/get-realtime-document.md) | `GET /v1/document` | [docs](https://docs.openregister.de/endpoint/document-realtime) |
| [Get Stored Document](actions/get-stored-document.md) | `GET /v1/document/:document_id` | [docs](https://docs.openregister.de/endpoint/document-stored) |
| [List Monitors](actions/list-monitors.md) | `GET /v1/monitor` | [docs](https://docs.openregister.de/endpoint/monitor-list) |
| [Search Companies](actions/search-companies.md) | `GET /v0/search/company` | [docs](https://docs.openregister.de/endpoint/search-company) |
| [Search Company By Website URL](actions/search-company-by-website-url.md) | `GET /v0/search/lookup` | [docs](https://docs.openregister.de/endpoint/search-lookup) |
| [Search Persons](actions/search-persons.md) | `POST /v1/search/person` | [docs](https://docs.openregister.de/endpoint/filter-person) |
