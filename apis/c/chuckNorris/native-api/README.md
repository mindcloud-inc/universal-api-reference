# Chuck Norris: Native API Reference

A consolidated summary of Chuck Norris's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://github.com/chucknorris-io/chuck-api
- **API base URL:** `https://api.chucknorris.io`

## Authentication

### Public API

This API does not require request authentication.

[Official authentication documentation](https://github.com/chucknorris-io/chuck-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Random Fact](actions/get-random-fact.md) | `GET /jokes/random` | [docs](https://github.com/chucknorris-io/chuck-api) |
| [List Fact Categories](actions/list-fact-categories.md) | `GET /jokes/categories` | [docs](https://github.com/chucknorris-io/chuck-api) |
| [Search Facts](actions/search-facts.md) | `GET /jokes/search` | [docs](https://github.com/chucknorris-io/chuck-api) |
