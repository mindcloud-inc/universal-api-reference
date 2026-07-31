# Owen Wilson Wow API: Native API Reference

A consolidated summary of Owen Wilson Wow API's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://github.com/amamenko/owen-wilson-wow-api
- **API base URL:** `https://owen-wilson-wow-api.onrender.com`

## Authentication

### No authentication

The public Owen Wilson Wow API requires no credentials.

This API does not require request authentication.

[Official authentication documentation](https://github.com/amamenko/owen-wilson-wow-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Ordered Wow](actions/get-ordered-wow.md) | `GET /wows/ordered/:index` | [docs](https://github.com/amamenko/owen-wilson-wow-api) |
| [Get Ordered Wow Range](actions/get-ordered-wow-range.md) | `GET /wows/ordered/:range` | [docs](https://github.com/amamenko/owen-wilson-wow-api) |
| [Get Random Wows](actions/get-random-wows.md) | `GET /wows/random` | [docs](https://github.com/amamenko/owen-wilson-wow-api) |
| [List Wow Directors](actions/list-wow-directors.md) | `GET /wows/directors` | [docs](https://github.com/amamenko/owen-wilson-wow-api) |
| [List Wow Movies](actions/list-wow-movies.md) | `GET /wows/movies` | [docs](https://github.com/amamenko/owen-wilson-wow-api) |
