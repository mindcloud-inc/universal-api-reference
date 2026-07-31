# Official Joke API: Native API Reference

A consolidated summary of Official Joke API's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://github.com/15Dkatz/official_joke_api
- **API base URL:** `https://official-joke-api.appspot.com`

## Authentication

### Public API

This API does not require request authentication.

[Official authentication documentation](https://github.com/15Dkatz/official_joke_api)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Joke by ID](actions/get-joke-by-id.md) | `GET /jokes/:id` | [docs](https://github.com/15Dkatz/official_joke_api) |
| [Get Random Joke](actions/get-random-joke.md) | `GET /jokes/random` | [docs](https://github.com/15Dkatz/official_joke_api) |
| [Get Random Joke by Type](actions/get-random-joke-by-type.md) | `GET /jokes/:type/random` | [docs](https://github.com/15Dkatz/official_joke_api) |
| [Get Random Jokes](actions/get-random-jokes.md) | `GET /jokes/random/:count` | [docs](https://github.com/15Dkatz/official_joke_api) |
| [Get Ten Jokes by Type](actions/get-ten-jokes-by-type.md) | `GET /jokes/:type/ten` | [docs](https://github.com/15Dkatz/official_joke_api) |
| [Get Ten Random Jokes](actions/get-ten-random-jokes.md) | `GET /jokes/ten` | [docs](https://github.com/15Dkatz/official_joke_api) |
| [List Joke Types](actions/list-joke-types.md) | `GET /types` | [docs](https://github.com/15Dkatz/official_joke_api) |
