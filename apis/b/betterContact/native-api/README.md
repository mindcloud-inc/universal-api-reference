# BetterContact: Native API Reference

A consolidated summary of BetterContact's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://doc.bettercontact.rocks/api-reference/
- **API base URL:** `https://app.bettercontact.rocks/api/v2`

## Authentication

### Header API Key

Use your BetterContact API key in the X-API-Key request header.

### Credentials

- **API Key:** `apiKey` · required · BetterContact API key sent in the X-API-Key request header.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://doc.bettercontact.rocks/api-reference/authentication)

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
| [Check Credit Balance](actions/check-credit-balance.md) | `GET /account` | [docs](https://doc.bettercontact.rocks/api-reference/endpoint/account) |
| [Create Enrichment](actions/create-enrichment.md) | `POST /async` | [docs](https://doc.bettercontact.rocks/api-reference/endpoint/create) |
| [Create Lead Finder Search](actions/create-lead-finder-search.md) | `POST /lead_finder/async` | [docs](https://doc.bettercontact.rocks/api-reference/endpoint/lead_finder_post) |
| [Get Enrichment Results](actions/get-enrichment-results.md) | `GET /async/:request_id` | [docs](https://doc.bettercontact.rocks/api-reference/endpoint/get) |
| [Get Lead Finder Search Results](actions/get-lead-finder-search-results.md) | `GET /lead_finder/async/:request_id` | [docs](https://doc.bettercontact.rocks/api-reference/endpoint/lead_finder_get) |
