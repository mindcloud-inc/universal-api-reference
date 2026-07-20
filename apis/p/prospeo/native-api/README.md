# Prospeo: Native API Reference

A consolidated summary of Prospeo's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://prospeo.io/api-docs/
- **API base URL:** `https://api.prospeo.io`

## Authentication

### API key

Authenticate Prospeo API requests with an API key.

### Credentials

- **API key:** `apiKey` · required

Send these headers with each API request:

```http
X-KEY: <apiKey>
```

[Official authentication documentation](https://prospeo.io/api-docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pagination.total_page`. The current page number is read from `pagination.current_page`.

## Pagination

Use `page` in the request body to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Enrich Companies](actions/bulk-enrich-companies.md) | `POST /bulk-enrich-company` | [docs](https://prospeo.io/api-docs/bulk-enrich-company) |
| [Bulk Enrich Persons](actions/bulk-enrich-persons.md) | `POST /bulk-enrich-person` | [docs](https://prospeo.io/api-docs/bulk-enrich-person) |
| [Bulk Enrich Persons with Mobile](actions/bulk-enrich-persons-with-mobile.md) | `POST /bulk-enrich-person` | [docs](https://prospeo.io/api-docs/bulk-enrich-person) |
| [Enrich Company](actions/enrich-company.md) | `POST /enrich-company` | [docs](https://prospeo.io/api-docs/enrich-company) |
| [Enrich Company by Search Result ID](actions/enrich-company-by-search-result-id.md) | `POST /enrich-company` | [docs](https://prospeo.io/api-docs/enrich-company) |
| [Enrich Person](actions/enrich-person.md) | `POST /enrich-person` | [docs](https://prospeo.io/api-docs/enrich-person) |
| [Enrich Person by Search Result ID](actions/enrich-person-by-search-result-id.md) | `POST /enrich-person` | [docs](https://prospeo.io/api-docs/enrich-person) |
| [Enrich Person with Mobile](actions/enrich-person-with-mobile.md) | `POST /enrich-person` | [docs](https://prospeo.io/api-docs/enrich-person) |
| [Enrich Person with Verified Email Only](actions/enrich-person-with-verified-email-only.md) | `POST /enrich-person` | [docs](https://prospeo.io/api-docs/enrich-person) |
| [Get Account Information](actions/get-account-information.md) | `GET /account-information` | [docs](https://prospeo.io/api-docs/account-information) |
| [Get Job Title Suggestions](actions/get-job-title-suggestions.md) | `POST /search-suggestions` | [docs](https://prospeo.io/api-docs/search-suggestions) |
| [Get Location Suggestions](actions/get-location-suggestions.md) | `POST /search-suggestions` | [docs](https://prospeo.io/api-docs/search-suggestions) |
| [Search Companies](actions/search-companies.md) | `POST /search-company` | [docs](https://prospeo.io/api-docs/search-company) |
| [Search Companies by Company List](actions/search-companies-by-company-list.md) | `POST /search-company` | [docs](https://prospeo.io/api-docs/search-company) |
| [Search Companies by Funding and Growth](actions/search-companies-by-funding-and-growth.md) | `POST /search-company` | [docs](https://prospeo.io/api-docs/search-company) |
| [Search Companies by Industry and Headcount](actions/search-companies-by-industry-and-headcount.md) | `POST /search-company` | [docs](https://prospeo.io/api-docs/search-company) |
| [Search Companies by Technology](actions/search-companies-by-technology.md) | `POST /search-company` | [docs](https://prospeo.io/api-docs/search-company) |
| [Search Persons](actions/search-persons.md) | `POST /search-person` | [docs](https://prospeo.io/api-docs/search-person) |
| [Search Persons by Company List](actions/search-persons-by-company-list.md) | `POST /search-person` | [docs](https://prospeo.io/api-docs/search-person) |
| [Search Persons by Department](actions/search-persons-by-department.md) | `POST /search-person` | [docs](https://prospeo.io/api-docs/search-person) |
| [Search Persons by Location](actions/search-persons-by-location.md) | `POST /search-person` | [docs](https://prospeo.io/api-docs/search-person) |
| [Search Persons by Title and Seniority](actions/search-persons-by-title-and-seniority.md) | `POST /search-person` | [docs](https://prospeo.io/api-docs/search-person) |
| [Search Persons with Verified Contact Details](actions/search-persons-with-verified-contact-details.md) | `POST /search-person` | [docs](https://prospeo.io/api-docs/search-person) |
