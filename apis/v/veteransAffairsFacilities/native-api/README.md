# Veterans Affairs Facilities: Native API Reference

A consolidated summary of Veterans Affairs Facilities's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://developer.va.gov/explore/api/va-facilities/docs
- **API base URL:** `https://sandbox-api.va.gov/services/va_facilities/v1`

## Authentication

### API Key

Authenticate requests with a VA API key sent in the apikey header.

### Credentials

- **VA API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.va.gov/explore/api/va-facilities/docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Nearby Facilities by Coordinates](actions/find-nearby-facilities-by-coordinates.md) | `GET /nearby` | [docs](https://developer.va.gov/explore/api/va-facilities/docs) |
| [Get Facilities by IDs](actions/get-facilities-by-ids.md) | `GET /facilities` | [docs](https://developer.va.gov/explore/api/va-facilities/docs) |
| [Get Facility](actions/get-facility.md) | `GET /facilities/:facilityId` | [docs](https://developer.va.gov/explore/api/va-facilities/docs) |
| [List Facility IDs](actions/list-facility-ids.md) | `GET /ids` | [docs](https://developer.va.gov/explore/api/va-facilities/docs) |
| [Search Facilities by Bounding Box](actions/search-facilities-by-bounding-box.md) | `GET /facilities` | [docs](https://developer.va.gov/explore/api/va-facilities/docs) |
| [Search Facilities by Coordinates](actions/search-facilities-by-coordinates.md) | `GET /facilities` | [docs](https://developer.va.gov/explore/api/va-facilities/docs) |
| [Search Facilities by State](actions/search-facilities-by-state.md) | `GET /facilities` | [docs](https://developer.va.gov/explore/api/va-facilities/docs) |
| [Search Facilities by ZIP Code](actions/search-facilities-by-zip-code.md) | `GET /facilities` | [docs](https://developer.va.gov/explore/api/va-facilities/docs) |
