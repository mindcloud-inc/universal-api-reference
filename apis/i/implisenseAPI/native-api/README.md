# Implisense: Native API Reference

A consolidated summary of Implisense's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.implisense.com/api/
- **OpenAPI specification:** https://docs.implisense.com/api/openapi.json
- **API base URL:** `https://german-company-data.p.rapidapi.com`

## Authentication

### RapidAPI Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-RapidAPI-Key: <apiKey>
```

[Official authentication documentation](https://docs.rapidapi.com/v2.0/docs/configuring-api-authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Company Data](actions/get-company-data.md) | `GET /companies/:id/data` | [docs](https://docs.implisense.com/api/) |
| [Get Company Data By Lookup](actions/get-company-data-by-lookup.md) | `POST /companies/data` | [docs](https://docs.implisense.com/api/) |
| [Get Company Events](actions/get-company-events.md) | `GET /companies/:id/events` | [docs](https://docs.implisense.com/api/) |
| [Get Company Events By Lookup](actions/get-company-events-by-lookup.md) | `POST /companies/events` | [docs](https://docs.implisense.com/api/) |
| [Get Company Financials](actions/get-company-financials.md) | `GET /companies/:id/financials` | [docs](https://docs.implisense.com/api/) |
| [Get Company Financials Availability](actions/get-company-financials-availability.md) | `GET /companies/:id/financials/exists` | [docs](https://docs.implisense.com/api/) |
| [Get Company Financials Availability By Lookup](actions/get-company-financials-availability-by-lookup.md) | `POST /companies/financials/exists` | [docs](https://docs.implisense.com/api/) |
| [Get Company Financials By Lookup](actions/get-company-financials-by-lookup.md) | `POST /companies/financials` | [docs](https://docs.implisense.com/api/) |
| [Get Company Jobs](actions/get-company-jobs.md) | `GET /companies/:id/jobs` | [docs](https://docs.implisense.com/api/) |
| [Get Company Jobs By Lookup](actions/get-company-jobs-by-lookup.md) | `POST /companies/jobs` | [docs](https://docs.implisense.com/api/) |
| [Get Company People](actions/get-company-people.md) | `GET /companies/:id/people` | [docs](https://docs.implisense.com/api/) |
| [Get Company People By Lookup](actions/get-company-people-by-lookup.md) | `POST /companies/people` | [docs](https://docs.implisense.com/api/) |
| [Get Suggestions](actions/get-suggestions.md) | `GET /suggest/:prefix` | [docs](https://docs.implisense.com/api/) |
| [Lookup Companies](actions/lookup-companies.md) | `POST /lookup` | [docs](https://docs.implisense.com/api/) |
| [Search Companies](actions/search-companies.md) | `POST /search` | [docs](https://docs.implisense.com/api/) |
