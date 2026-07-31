# SWAPI: Native API Reference

A consolidated summary of SWAPI's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://swapi.dev/api/
- **API base URL:** `https://swapi.dev/api`

## Authentication

### No authentication

This API does not require request authentication.

[Official authentication documentation](https://swapi.dev/api/)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Film](actions/get-film.md) | `GET /films/:id/` | [docs](https://swapi.dev/api/) |
| [Get Person](actions/get-person.md) | `GET /people/:id/` | [docs](https://swapi.dev/api/) |
| [Get Planet](actions/get-planet.md) | `GET /planets/:id/` | [docs](https://swapi.dev/api/) |
| [Get Species](actions/get-species.md) | `GET /species/:id/` | [docs](https://swapi.dev/api/) |
| [Get Starship](actions/get-starship.md) | `GET /starships/:id/` | [docs](https://swapi.dev/api/) |
| [Get Vehicle](actions/get-vehicle.md) | `GET /vehicles/:id/` | [docs](https://swapi.dev/api/) |
| [List Films](actions/list-films.md) | `GET /films/` | [docs](https://swapi.dev/api/) |
| [List People](actions/list-people.md) | `GET /people/` | [docs](https://swapi.dev/api/) |
| [List Planets](actions/list-planets.md) | `GET /planets/` | [docs](https://swapi.dev/api/) |
| [List Species](actions/list-species.md) | `GET /species/` | [docs](https://swapi.dev/api/) |
| [List Starships](actions/list-starships.md) | `GET /starships/` | [docs](https://swapi.dev/api/) |
| [List Vehicles](actions/list-vehicles.md) | `GET /vehicles/` | [docs](https://swapi.dev/api/) |
