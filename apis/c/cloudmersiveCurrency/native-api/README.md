# Cloudmersive Currency: Native API Reference

A consolidated summary of Cloudmersive Currency's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://api.cloudmersive.com/docs/currency.asp
- **API base URL:** `https://api.cloudmersive.com`

## Authentication

### Cloudmersive API Key

Cloudmersive API key authentication. The key is sent as the Apikey request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Apikey: <apiKey>
```

[Official authentication documentation](https://api.cloudmersive.com/docs/currency.asp)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Currency](actions/convert-currency.md) | `POST /currency/exchange-rates/convert/:source/to/:destination` | [docs](https://api.cloudmersive.com/docs/currency.asp#operation--currency-exchange-rates-convert-source-to-destination-post) |
| [Get Exchange Rate](actions/get-exchange-rate.md) | `POST /currency/exchange-rates/get/:source/to/:destination` | [docs](https://api.cloudmersive.com/docs/currency.asp#operation--currency-exchange-rates-get-source-to-destination-post) |
| [List Available Currencies](actions/list-available-currencies.md) | `POST /currency/exchange-rates/list-available` | [docs](https://api.cloudmersive.com/docs/currency.asp#operation--currency-exchange-rates-list-available-post) |
