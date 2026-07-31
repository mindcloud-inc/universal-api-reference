# Amiibo API: Native API Reference

A consolidated summary of Amiibo API's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://github.com/N3evin/AmiiboAPI
- **API base URL:** `https://amiiboapi.com`

## Authentication

### No authentication

The archived AmiiboAPI source exposes public read endpoints without credentials.

This API does not require request authentication.

[Official authentication documentation](https://github.com/N3evin/AmiiboAPI)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 250 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Amiibo by ID](actions/get-amiibo-by-id.md) | `GET /api/amiibo/` | [docs](https://github.com/N3evin/AmiiboAPI) |
| [Get Amiibo Last Updated](actions/get-amiibo-last-updated.md) | `GET /api/lastupdated/` | [docs](https://github.com/N3evin/AmiiboAPI) |
| [Get Amiibo Series by Key](actions/get-amiibo-series-by-key.md) | `GET /api/amiiboseries/` | [docs](https://github.com/N3evin/AmiiboAPI) |
| [Get Amiibo Type by Key](actions/get-amiibo-type-by-key.md) | `GET /api/type/` | [docs](https://github.com/N3evin/AmiiboAPI) |
| [Get Character by Key](actions/get-character-by-key.md) | `GET /api/character/` | [docs](https://github.com/N3evin/AmiiboAPI) |
| [Get Detailed Amiibo by Head and Tail](actions/get-detailed-amiibo-by-head-and-tail.md) | `GET /api/amiibofull/` | [docs](https://github.com/N3evin/AmiiboAPI) |
| [Get Game Series by Key](actions/get-game-series-by-key.md) | `GET /api/gameseries/` | [docs](https://github.com/N3evin/AmiiboAPI) |
| [List Amiibo Series](actions/list-amiibo-series.md) | `GET /api/amiiboseries/` | [docs](https://github.com/N3evin/AmiiboAPI) |
| [List Amiibo Type](actions/list-amiibo-type.md) | `GET /api/type/` | [docs](https://github.com/N3evin/AmiiboAPI) |
| [List Character](actions/list-character.md) | `GET /api/character/` | [docs](https://github.com/N3evin/AmiiboAPI) |
| [List Game Series](actions/list-game-series.md) | `GET /api/gameseries/` | [docs](https://github.com/N3evin/AmiiboAPI) |
| [Search Amiibo](actions/search-amiibo.md) | `GET /api/amiibo/` | [docs](https://github.com/N3evin/AmiiboAPI) |
