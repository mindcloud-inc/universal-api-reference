# GoT Quotes: Native API Reference

A consolidated summary of GoT Quotes's API configuration and 8 documented operations.

- **API base URL:** `https://api.gameofthronesquotes.xyz`

## Authentication

### No authentication

This API does not require request authentication.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Character](actions/get-character.md) | `GET /v1/character/:slug` | [docs](https://github.com/shevabam/game-of-thrones-quotes-api) |
| [Get House](actions/get-house.md) | `GET /v1/house/:slug` | [docs](https://github.com/shevabam/game-of-thrones-quotes-api) |
| [Get Random Quote](actions/get-random-quote.md) | `GET /v1/random` | [docs](https://github.com/shevabam/game-of-thrones-quotes-api) |
| [Get Random Quote by Character](actions/get-random-quote-by-character.md) | `GET /v1/author/:character` | [docs](https://github.com/shevabam/game-of-thrones-quotes-api) |
| [Get Random Quotes](actions/get-random-quotes.md) | `GET /v1/random/:count` | [docs](https://github.com/shevabam/game-of-thrones-quotes-api) |
| [Get Random Quotes by Character](actions/get-random-quotes-by-character.md) | `GET /v1/author/:character/:count` | [docs](https://github.com/shevabam/game-of-thrones-quotes-api) |
| [List Characters](actions/list-characters.md) | `GET /v1/characters` | [docs](https://github.com/shevabam/game-of-thrones-quotes-api) |
| [List Houses](actions/list-houses.md) | `GET /v1/houses` | [docs](https://github.com/shevabam/game-of-thrones-quotes-api) |
