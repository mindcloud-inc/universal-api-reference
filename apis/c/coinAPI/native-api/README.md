# CoinAPI: Native API Reference

A consolidated summary of CoinAPI's API configuration, with links to official documentation.

- **Official docs:** https://docs.coinapi.io/market-data/
- **OpenAPI specification:** https://raw.githubusercontent.com/api-bricks/api-bricks-sdk/master/coinapi/market-data-api-rest/spec/openapi.json
- **API base URL:** `https://rest.coinapi.io`

## Authentication

### API Key

Authenticate with a CoinAPI API key. The wrapper sends it in the documented raw Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.coinapi.io/market-data/authentication)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100000). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
