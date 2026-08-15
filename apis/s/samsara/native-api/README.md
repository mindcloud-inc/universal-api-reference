# Samsara: Native API Reference

A consolidated summary of Samsara's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://developers.samsara.com/reference
- **OpenAPI specification:** https://developers.samsara.com/openapi/samsara-api.json
- **API base URL:** `https://api.samsara.com/`

## Authentication

### API Token

Authenticate with a Samsara API token. OAuth 2.0 is recommended for Marketplace installations.

### Credentials

- **API Token:** `apiToken` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiToken>
```

[Official authentication documentation](https://developers.samsara.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Response data is read from `data`. The next-page cursor is read from `pagination.endCursor`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–512). Use `after` in the query string as the pagination cursor.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Driver](actions/create-driver.md) | `POST fleet/drivers` |  |
| [Get Address](actions/get-address.md) | `GET addresses/:id` | [docs](https://developers.samsara.com/reference/getaddress) |
| [Get Driver](actions/get-driver.md) | `GET fleet/drivers/:id` | [docs](https://developers.samsara.com/reference/getdriver) |
| [Get Equipment](actions/get-equipment.md) | `GET fleet/equipment/:id` | [docs](https://developers.samsara.com/reference/getequipment) |
| [Get HOS Clocks](actions/get-hos-clocks.md) | `GET fleet/hos/clocks` | [docs](https://developers.samsara.com/reference/gethosclocks) |
| [Get Organization](actions/get-organization.md) | `GET me` | [docs](https://developers.samsara.com/reference/getorganizationinfo) |
| [Get Tag](actions/get-tag.md) | `GET tags/:id` | [docs](https://developers.samsara.com/reference/gettag) |
| [Get Trailer](actions/get-trailer.md) | `GET fleet/trailers/:id` | [docs](https://developers.samsara.com/reference/gettrailer) |
| [Get User](actions/get-user.md) | `GET users/:id` | [docs](https://developers.samsara.com/reference/getuser) |
| [Get Vehicle](actions/get-vehicle.md) | `GET fleet/vehicles/:id` | [docs](https://developers.samsara.com/reference/getvehicle) |
| [Get Vehicle Locations](actions/get-vehicle-locations.md) | `GET fleet/vehicles/locations` | [docs](https://developers.samsara.com/reference/getvehiclelocations) |
| [Get Vehicle Stats](actions/get-vehicle-stats.md) | `GET fleet/vehicles/stats` | [docs](https://developers.samsara.com/reference/getvehiclestats) |
| [List Addresses](actions/list-addresses.md) | `GET addresses` | [docs](https://developers.samsara.com/reference/listaddresses) |
| [List Drivers](actions/list-all-drivers.md) | `GET fleet/drivers` | [docs](https://developers.samsara.com/reference/listdrivers) |
| [List Tags](actions/list-all-tags1.md) | `GET tags` | [docs](https://developers.samsara.com/reference/listtags) |
| [List Vehicles](actions/list-all-vehicles.md) | `GET fleet/vehicles` | [docs](https://developers.samsara.com/reference/listvehicles) |
| [List Assets](actions/list-assets.md) | `GET assets` | [docs](https://developers.samsara.com/reference/listassets) |
| [List Driver-Vehicle Assignments](actions/list-driver-vehicle-assignments.md) | `GET fleet/driver-vehicle-assignments` | [docs](https://developers.samsara.com/reference/getdrivervehicleassignments) |
| [List Equipment](actions/list-equipment.md) | `GET fleet/equipment` | [docs](https://developers.samsara.com/reference/listequipment) |
| [List Routes](actions/list-routes.md) | `GET fleet/routes` | [docs](https://developers.samsara.com/reference/fetchroutes) |
| [List Trailers](actions/list-trailers.md) | `GET fleet/trailers` | [docs](https://developers.samsara.com/reference/listtrailers) |
| [List User Roles](actions/list-user-roles.md) | `GET user-roles` | [docs](https://developers.samsara.com/reference/listuserroles) |
| [List Users](actions/list-users.md) | `GET users` | [docs](https://developers.samsara.com/reference/listusers) |
| [Stream DVIR Defects](actions/stream-dvir-defects.md) | `GET defects/stream` | [docs](https://developers.samsara.com/reference/streamdefects) |
| [Stream DVIRs](actions/stream-dvirs.md) | `GET dvirs/stream` | [docs](https://developers.samsara.com/reference/getdvirs) |
| [Update Driver](actions/update-driver.md) | `PATCH fleet/drivers/:driverId` |  |
