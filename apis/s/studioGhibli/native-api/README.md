# Studio Ghibli: Native API Reference

A consolidated summary of Studio Ghibli's API configuration and 10 documented operations.

- **API base URL:** `https://ghibliapi.vercel.app`

## Authentication

### No authentication

The Studio Ghibli API is publicly accessible without authentication.

This API does not require request authentication.

## Pagination

Use `limit` in the query string to set the page size (default 50; maximum 250).

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Film by ID](actions/get-film-by-id.md) | `GET /films/:id` | [docs](https://github.com/deywersonp/ghibliapi/blob/master/public/swagger.yaml) |
| [Get Location by ID](actions/get-location-by-id.md) | `GET /locations/:id` | [docs](https://github.com/deywersonp/ghibliapi/blob/master/public/swagger.yaml) |
| [Get Person by ID](actions/get-person-by-id.md) | `GET /people/:id` | [docs](https://github.com/deywersonp/ghibliapi/blob/master/public/swagger.yaml) |
| [Get Species by ID](actions/get-species-by-id.md) | `GET /species/:id` | [docs](https://github.com/deywersonp/ghibliapi/blob/master/public/swagger.yaml) |
| [Get Vehicle by ID](actions/get-vehicle-by-id.md) | `GET /vehicles/:id` | [docs](https://github.com/deywersonp/ghibliapi/blob/master/public/swagger.yaml) |
| [List Films](actions/list-films.md) | `GET /films` | [docs](https://github.com/deywersonp/ghibliapi/blob/master/public/swagger.yaml) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://github.com/deywersonp/ghibliapi/blob/master/public/swagger.yaml) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://github.com/deywersonp/ghibliapi/blob/master/public/swagger.yaml) |
| [List Species](actions/list-species.md) | `GET /species` | [docs](https://github.com/deywersonp/ghibliapi/blob/master/public/swagger.yaml) |
| [List Vehicles](actions/list-vehicles.md) | `GET /vehicles` | [docs](https://github.com/deywersonp/ghibliapi/blob/master/public/swagger.yaml) |
