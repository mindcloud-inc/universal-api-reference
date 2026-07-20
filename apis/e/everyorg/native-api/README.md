# Every.org: Native API Reference

A consolidated summary of Every.org's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.every.org/docs/intro
- **API base URL:** `https://partners.every.org/v0.2`

## Authentication

### API Key

Use a public API key for public endpoints and a private key for privileged requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.every.org/docs/endpoints/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `pagination.pages`. The current page number is read from `pagination.page`.

## Pagination

Use `take` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Browse Nonprofits](actions/browse-nonprofits.md) | `GET /browse/:cause` | [docs](https://docs.every.org/docs/endpoints/nonprofit-search#get-v02browsecause) |
| [Create Fundraiser](actions/create-fundraiser.md) | `POST /fundraiser` | [docs](https://docs.every.org/docs/endpoints/fundraisers#post-v02fundraiser) |
| [Get Fundraiser](actions/get-fundraiser.md) | `GET /nonprofit/:nonprofitIdentifier/fundraiser/:fundraiserIdentifier` | [docs](https://docs.every.org/docs/endpoints/fundraisers#get-v02nonprofitnonprofitidentifierfundraiserfundraiseridentifier) |
| [Get Fundraiser Raised](actions/get-fundraiser-raised.md) | `GET /nonprofit/:nonprofitIdentifier/fundraiser/:fundraiserIdentifier/raised` | [docs](https://docs.every.org/docs/endpoints/fundraisers#get-v02nonprofitnonprofitidentifierfundraiserfundraiseridentifierraised) |
| [Get Nonprofit](actions/get-nonprofit.md) | `GET /nonprofit/:identifier` | [docs](https://docs.every.org/docs/endpoints/nonprofit-search#get-v02nonprofitidentifier) |
| [Search Nonprofits](actions/search-nonprofits.md) | `GET /search/:searchTerm` | [docs](https://docs.every.org/docs/endpoints/nonprofit-search#get-v02searchsearchterm) |
