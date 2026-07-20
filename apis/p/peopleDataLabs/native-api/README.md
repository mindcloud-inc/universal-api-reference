# People Data Labs: Native API Reference

A consolidated summary of People Data Labs's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.peopledatalabs.com/
- **API base URL:** `https://api.peopledatalabs.com/v5`

## Authentication

### API Key (Header Only)

Authenticate with your People Data Labs API key using the documented X-Api-Key header only.

### Credentials

- **API Key:** `apiKey` · required · Your People Data Labs Active Key.

[Official authentication documentation](https://docs.peopledatalabs.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The next-page cursor is read from `scroll_token`.

## Pagination

Use `size` in the query string to set the page size (default 10; accepted range 1–100). Use `scroll_token` in the query string as the pagination cursor.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete](actions/autocomplete.md) | `GET /autocomplete` | [docs](https://docs.peopledatalabs.com/docs/reference-autocomplete-api) |
| [Bulk Enrich Companies](actions/bulk-enrich-companies.md) | `POST /company/enrich/bulk` | [docs](https://docs.peopledatalabs.com/docs/bulk-company-enrichment-api) |
| [Bulk Enrich People](actions/bulk-enrich-people.md) | `POST /person/bulk` | [docs](https://docs.peopledatalabs.com/docs/bulk-enrichment-api) |
| [Clean Company](actions/clean-company.md) | `GET /company/clean` | [docs](https://docs.peopledatalabs.com/docs/cleaner-apis-reference#company-cleaner-api-companyclean) |
| [Clean Location](actions/clean-location.md) | `GET /location/clean` | [docs](https://docs.peopledatalabs.com/docs/cleaner-apis-reference#location-cleaner-api-locationclean) |
| [Clean School](actions/clean-school.md) | `GET /school/clean` | [docs](https://docs.peopledatalabs.com/docs/cleaner-apis-reference#school-cleaner-api-schoolclean) |
| [Enrich Company](actions/enrich-company.md) | `GET /company/enrich` | [docs](https://docs.peopledatalabs.com/docs/reference-company-enrichment-api) |
| [Enrich IP](actions/enrich-ip.md) | `GET /ip/enrich` | [docs](https://docs.peopledatalabs.com/docs/reference-ip-enrichment-api) |
| [Enrich Person](actions/enrich-person.md) | `GET /person/enrich` | [docs](https://docs.peopledatalabs.com/docs/reference-person-enrichment-api) |
| [Search Companies](actions/search-companies.md) | `GET /company/search` | [docs](https://docs.peopledatalabs.com/docs/reference-company-search-api) |
| [Search People](actions/search-people.md) | `GET /person/search` | [docs](https://docs.peopledatalabs.com/docs/reference-person-search-api) |
