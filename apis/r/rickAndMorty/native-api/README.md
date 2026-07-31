# Rick and Morty: Native API Reference

A consolidated summary of Rick and Morty's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://rickandmortyapi.com/documentation
- **API base URL:** `https://rickandmortyapi.com/api`

## Authentication

### No authentication

The public Rick and Morty REST API requires no credentials.

This API does not require request authentication.

[Official authentication documentation](https://rickandmortyapi.com/documentation)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Character](actions/get-character.md) | `GET /character/:id` | [docs](https://rickandmortyapi.com/documentation) |
| [Get Episode](actions/get-episode.md) | `GET /episode/:id` | [docs](https://rickandmortyapi.com/documentation) |
| [Get Location](actions/get-location.md) | `GET /location/:id` | [docs](https://rickandmortyapi.com/documentation) |
| [List Characters](actions/list-characters.md) | `GET /character` | [docs](https://rickandmortyapi.com/documentation) |
| [List Episodes](actions/list-episodes.md) | `GET /episode` | [docs](https://rickandmortyapi.com/documentation) |
| [List Locations](actions/list-locations.md) | `GET /location` | [docs](https://rickandmortyapi.com/documentation) |
