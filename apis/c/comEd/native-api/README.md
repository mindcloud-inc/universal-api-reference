# ComEd: Native API Reference

A consolidated summary of ComEd's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://hourlypricing.comed.com/hp-api/
- **API base URL:** `https://hourlypricing.comed.com`

## Authentication

### No Authentication

This public ComEd Hourly Pricing API does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://hourlypricing.comed.com/comed-hourly-pricing-apis-terms-of-service/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current Hour Average](actions/get-current-hour-average.md) | `GET /api?type=currenthouraverage&format=json` | [docs](https://hourlypricing.comed.com/hp-api/) |
| [Get Latest 5-Minute Prices](actions/get-latest5-minute-prices.md) | `GET /api?type=5minutefeed&format=json` | [docs](https://hourlypricing.comed.com/hp-api/) |
| [Get 5-Minute Prices By Time Range](actions/get5-minute-prices-by-time-range.md) | `GET /api` | [docs](https://hourlypricing.comed.com/hp-api/) |
