# Breaking Bad Quotes: Native API Reference

A consolidated summary of Breaking Bad Quotes's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://github.com/shevabam/breaking-bad-quotes
- **API base URL:** `https://api.breakingbadquotes.xyz`

## Authentication

### No authentication

The public Breaking Bad Quotes API requires no authentication.

This API does not require request authentication.

[Official authentication documentation](https://breakingbadquotes.xyz/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Random Quote](actions/get-random-quote.md) | `GET /v1/quotes` | [docs](https://github.com/shevabam/breaking-bad-quotes) |
| [Get Random Quotes](actions/get-random-quotes.md) | `GET /v1/quotes/:count` | [docs](https://github.com/shevabam/breaking-bad-quotes) |
