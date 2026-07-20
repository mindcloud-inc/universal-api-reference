# Ron Swanson Quotes: Native API Reference

A consolidated summary of Ron Swanson Quotes's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://github.com/jamesseanwright/ron-swanson-quotes
- **API base URL:** `https://ron-swanson-quotes.herokuapp.com/v2`

## Authentication

### No Auth

Ron Swanson Quotes is a public unauthenticated REST API.

This API does not require request authentication.

[Official authentication documentation](https://github.com/jamesseanwright/ron-swanson-quotes)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Quotes](actions/get-quotes.md) | `GET /quotes/:count` | [docs](https://github.com/jamesseanwright/ron-swanson-quotes#apis) |
| [Get Random Quote](actions/get-random-quote.md) | `GET /quotes` | [docs](https://github.com/jamesseanwright/ron-swanson-quotes#apis) |
| [Search Quotes](actions/search-quotes.md) | `GET /quotes/search/:term` | [docs](https://github.com/jamesseanwright/ron-swanson-quotes#apis) |
