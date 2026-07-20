# Parklio: Native API Reference

A consolidated summary of Parklio's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.parklio.com/api
- **OpenAPI specification:** https://api.parklio.com/api-json
- **API base URL:** `https://api.parklio.com`

## Authentication

### API Key

Authenticate Parklio requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.parklio.com/zapier)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `size` in the query string to set the page size (default 200). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Product Counts](actions/get-account-product-counts.md) | `GET /v2/accounts/product-counts` | [docs](https://api.parklio.com/api#/ACCOUNTS/AccountsController_getProductCountForProfile) |
| [Get Lot](actions/get-lot.md) | `GET /v2/lots/:id` | [docs](https://api.parklio.com/api#/LOTS/LotsController_findOne) |
| [Get Zone](actions/get-zone.md) | `GET /v2/zones/:id` | [docs](https://api.parklio.com/api#/ZONES/ZonesController_findOne) |
| [List Devices](actions/list-devices.md) | `GET /v2/devices` | [docs](https://api.parklio.com/api#/DEVICES/DevicesController_findAll) |
| [List Gates](actions/list-gates.md) | `GET /v2/gates` | [docs](https://api.parklio.com/api#/GATES/GatesController_findAll) |
| [List Gateways](actions/list-gateways.md) | `GET /v2/gateways` | [docs](https://api.parklio.com/api#/GATEWAYS/GatewaysController_findAll) |
| [List Groups](actions/list-groups.md) | `GET /v2/groups` | [docs](https://api.parklio.com/api#/GROUPS/GroupsController_findAll) |
| [List Key Logs](actions/list-key-logs.md) | `GET /v2/key-logs` | [docs](https://api.parklio.com/api#/KEY%20LOGS/KeyLogsController_findAll) |
| [List Lot Entries](actions/list-lot-entries.md) | `GET /v2/lot-entries` | [docs](https://api.parklio.com/api#/LOT%20ENTRIES/LotEntriesController_findAll) |
| [List Lots](actions/list-lots.md) | `GET /v2/lots` | [docs](https://api.parklio.com/api#/LOTS/LotsController_findAll) |
| [List Parking Places](actions/list-parking-places.md) | `GET /v2/parking-places` | [docs](https://api.parklio.com/api#/PARKING%20PLACES/ParkingPlacesController_findAll) |
| [List Product Errors](actions/list-product-errors.md) | `GET /v2/products/errors` | [docs](https://api.parklio.com/api#/PRODUCTS/ProductsController_findAllProductErrors) |
| [List Products](actions/list-products.md) | `GET /v2/products` | [docs](https://api.parklio.com/api#/PRODUCTS/ProductsController_findAll) |
| [List QR Codes](actions/list-qr-codes.md) | `GET /v2/qr-codes` | [docs](https://api.parklio.com/api#/QR%20CODES/QrCodesController_findAll) |
| [List Tariffs](actions/list-tariffs.md) | `GET /v2/tariffs` | [docs](https://api.parklio.com/api#/TARIFFS/TariffsController_findAll) |
| [List Terminals](actions/list-terminals.md) | `GET /v2/terminals` | [docs](https://api.parklio.com/api#/TERMINALS/TerminalsController_findAll) |
| [List Weblinks](actions/list-weblinks.md) | `GET /v2/weblinks` | [docs](https://api.parklio.com/api#/WEBLINKS/WeblinksController_findAll) |
| [List Zones](actions/list-zones.md) | `GET /v2/zones` | [docs](https://api.parklio.com/api#/ZONES/ZonesController_findAll) |
| [Update Lot Description](actions/update-lot-description.md) | `PATCH /v2/lots/:id` | [docs](https://api.parklio.com/api#/LOTS/LotsController_update) |
| [Update Zone Description](actions/update-zone-description.md) | `PATCH /v2/zones/:id` | [docs](https://api.parklio.com/api#/ZONES/ZonesController_update) |
