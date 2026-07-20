# Advanced Scraper: Native API Reference

A consolidated summary of Advanced Scraper's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://marketplace.apilayer.com/adv_scraper-api
- **API base URL:** `https://api.apilayer.com/adv_scraper`

## Authentication

### APILayer API Key

Authenticate to APILayer Advanced Scraper with the API key header named apikey.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://marketplace.apilayer.com/adv_scraper-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Scrape URL](actions/scrape-url.md) | `GET /scraper` | [docs](https://marketplace.apilayer.com/adv_scraper-api) |
