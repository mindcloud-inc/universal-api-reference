# Whisky Hunter: Native API Reference

A consolidated summary of Whisky Hunter's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://whiskyhunter.net/api/
- **API base URL:** `https://whiskyhunter.net/api`

## Authentication

### No Authentication

Whisky Hunter public API endpoints do not require provider credentials.

This API does not require request authentication.

[Official authentication documentation](https://whiskyhunter.net/api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get API Schema](actions/get-api-schema.md) | `GET /` | [docs](https://whiskyhunter.net/api/) |
| [Get Auction Market Data](actions/get-auction-market-data.md) | `GET /auction_data/[:slug]/` | [docs](https://whiskyhunter.net/api/) |
| [Get Distillery Market Data](actions/get-distillery-market-data.md) | `GET /distillery_data/[:slug]/` | [docs](https://whiskyhunter.net/api/) |
| [List Auction Market Data](actions/list-auction-market-data.md) | `GET /auctions_data/` | [docs](https://whiskyhunter.net/api/) |
| [List Auctions](actions/list-auctions.md) | `GET /auctions_info` | [docs](https://whiskyhunter.net/api/) |
| [List Distilleries](actions/list-distilleries.md) | `GET /distilleries_info/` | [docs](https://whiskyhunter.net/api/) |
