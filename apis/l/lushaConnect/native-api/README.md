# Lusha Connect: Native API Reference

A consolidated summary of Lusha Connect's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://docs.lusha.com/apis/openapi
- **API base URL:** `https://api.lusha.com`

## Authentication

### API Key

Authenticate requests with the Lusha account API key sent in the api_key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.lusha.com/apis/openapi/section/how-to-authenticate)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Usage](actions/get-account-usage.md) | `GET /account/usage` | [docs](https://docs.lusha.com/apis/openapi/credit-usage/getaccountusagestats) |
| [Search Companies](actions/search-companies.md) | `POST /v2/company` | [docs](https://docs.lusha.com/apis/openapi/enrichment/searchsinglecompanyv2) |
| [Search Contacts](actions/search-contacts.md) | `POST /v2/person` | [docs](https://docs.lusha.com/apis/openapi/enrichment/searchsinglecontact) |
| [Search Prospecting Companies](actions/search-prospecting-companies.md) | `POST /prospecting/company/search` | [docs](https://docs.lusha.com/apis/openapi/prospecting-search-and-enrich/searchprospectingcompanies) |
| [Search Prospecting Contacts](actions/search-prospecting-contacts.md) | `POST /prospecting/contact/search` | [docs](https://docs.lusha.com/apis/openapi/prospecting-search-and-enrich/searchprospectingcontacts) |
