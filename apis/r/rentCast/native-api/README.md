# RentCast: Native API Reference

A consolidated summary of RentCast's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://developers.rentcast.io/reference
- **OpenAPI specification:** https://raw.githubusercontent.com/RentCast/api-resources/main/openapi-spec/rentcast_api_openapi_spec_v1.json
- **API base URL:** `https://api.rentcast.io/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://developers.rentcast.io/reference/getting-started-guide)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (accepted range 1–500). Use `offset` in the query string as the record offset.

## Filtering

Send filters in the query string. Supported operators: `between`, `eq`, `includes`.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Market Statistics](actions/get-market-statistics.md) | `GET /markets` | [docs](https://developers.rentcast.io/reference/market-statistics) |
| [Get Property Record by ID](actions/get-property-record-by-id.md) | `GET /properties/:id` | [docs](https://developers.rentcast.io/reference/property-record-by-id) |
| [Get Rent Estimate](actions/get-rent-estimate.md) | `GET /avm/rent/long-term` | [docs](https://developers.rentcast.io/reference/rent-estimate-long-term) |
| [Get Rental Listing by ID](actions/get-rental-listing-by-id.md) | `GET /listings/rental/long-term/:id` | [docs](https://developers.rentcast.io/reference/rental-listing-long-term-by-id) |
| [Get Sale Listing by ID](actions/get-sale-listing-by-id.md) | `GET /listings/sale/:id` | [docs](https://developers.rentcast.io/reference/sale-listing-by-id) |
| [Get Value Estimate](actions/get-value-estimate.md) | `GET /avm/value` | [docs](https://developers.rentcast.io/reference/value-estimate) |
| [List Random Property Records](actions/list-random-property-records.md) | `GET /properties/random` | [docs](https://developers.rentcast.io/reference/property-records-random) |
| [Search Property Records](actions/search-property-records.md) | `GET /properties` | [docs](https://developers.rentcast.io/reference/property-records) |
| [Search Rental Listings](actions/search-rental-listings.md) | `GET /listings/rental/long-term` | [docs](https://developers.rentcast.io/reference/rental-listings-long-term) |
| [Search Sale Listings](actions/search-sale-listings.md) | `GET /listings/sale` | [docs](https://developers.rentcast.io/reference/sale-listings) |
