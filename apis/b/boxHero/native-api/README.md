# BoxHero: Native API Reference

A consolidated summary of BoxHero's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://rest.boxhero-app.com/docs/api
- **API base URL:** `https://rest.boxhero-app.com`

## Authentication

### API Token

Connect with a BoxHero API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs-en.boxhero.io/integrations/open-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 0–100). Use `cursor` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | `POST /v1/items` | [docs](https://rest.boxhero-app.com/docs/api#/items/BarcodesController_createBarcode) |
| [Create Item Attribute](actions/create-item-attribute.md) | `POST /v1/item-attrs` | [docs](https://rest.boxhero-app.com/docs/api#/item-attrs/BarcodeAttrsController_createAttr) |
| [Create Location](actions/create-location.md) | `POST /v1/locations` | [docs](https://rest.boxhero-app.com/docs/api#/locations/LocationsController_createLocation) |
| [Create Location Transaction](actions/create-location-transaction.md) | `POST /v1/location-txs` | [docs](https://rest.boxhero-app.com/docs/api#/transactions/LocationTxsController_createTx) |
| [Create Partner](actions/create-partner.md) | `POST /v1/partners` | [docs](https://rest.boxhero-app.com/docs/api#/partners/VendorsController_createVendor) |
| [Delete Item](actions/delete-item.md) | `DELETE /v1/items/:item_id` | [docs](https://rest.boxhero-app.com/docs/api#/items/BarcodesController_deleteBarcode) |
| [Get Item](actions/get-item.md) | `GET /v1/items/:item_id` | [docs](https://rest.boxhero-app.com/docs/api#/items/BarcodesController_getBarcode) |
| [Get Item Attribute](actions/get-item-attribute.md) | `GET /v1/item-attrs/:attr_id` | [docs](https://rest.boxhero-app.com/docs/api#/item-attrs/BarcodeAttrsController_getAttr) |
| [Get Linked Team](actions/get-linked-team.md) | `GET /v1/teams/linked` | [docs](https://rest.boxhero-app.com/docs/api#/teams/TeamsController_getCurrentTeam) |
| [Get Location](actions/get-location.md) | `GET /v1/locations/:location_id` | [docs](https://rest.boxhero-app.com/docs/api#/locations/LocationsController_getLocation) |
| [Get Location Transaction](actions/get-location-transaction.md) | `GET /v1/location-txs/:tx_id` | [docs](https://rest.boxhero-app.com/docs/api#/transactions/LocationTxsController_getTx) |
| [Get Member](actions/get-member.md) | `GET /v1/members/:member_id` | [docs](https://rest.boxhero-app.com/docs/api#/members/MembersController_getMember) |
| [Get Partner](actions/get-partner.md) | `GET /v1/partners/:partner_id` | [docs](https://rest.boxhero-app.com/docs/api#/partners/VendorsController_getVendor) |
| [List Item Attributes](actions/list-item-attributes.md) | `GET /v1/item-attrs` | [docs](https://rest.boxhero-app.com/docs/api#/item-attrs/BarcodeAttrsController_getAttrs) |
| [List Items](actions/list-items.md) | `GET /v1/items` | [docs](https://rest.boxhero-app.com/docs/api#/items/BarcodesController_getBarcodes) |
| [List Location Transactions](actions/list-location-transactions.md) | `GET /v1/location-txs` | [docs](https://rest.boxhero-app.com/docs/api#/transactions/LocationTxsController_getLocationTxs) |
| [List Locations](actions/list-locations.md) | `GET /v1/locations` | [docs](https://rest.boxhero-app.com/docs/api#/locations/LocationsController_getLocations) |
| [List Members](actions/list-members.md) | `GET /v1/members` | [docs](https://rest.boxhero-app.com/docs/api#/members/MembersController_getMembers) |
| [List Partners](actions/list-partners.md) | `GET /v1/partners` | [docs](https://rest.boxhero-app.com/docs/api#/partners/VendorsController_getVendors) |
| [Update Item](actions/update-item.md) | `PUT /v1/items/:item_id` | [docs](https://rest.boxhero-app.com/docs/api#/items/BarcodesController_editBarcode) |
| [Update Item Attribute](actions/update-item-attribute.md) | `PUT /v1/item-attrs/:attr_id` | [docs](https://rest.boxhero-app.com/docs/api#/item-attrs/BarcodeAttrsController_updateAttr) |
| [Update Location](actions/update-location.md) | `PUT /v1/locations/:location_id` | [docs](https://rest.boxhero-app.com/docs/api#/locations/LocationsController_updateLocation) |
| [Update Location Transaction](actions/update-location-transaction.md) | `PUT /v1/location-txs/:tx_id` | [docs](https://rest.boxhero-app.com/docs/api#/transactions/LocationTxsController_updateTx) |
| [Update Partner](actions/update-partner.md) | `PUT /v1/partners/:partner_id` | [docs](https://rest.boxhero-app.com/docs/api#/partners/VendorsController_updateVendor) |
