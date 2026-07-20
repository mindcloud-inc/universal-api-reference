# Bookvault: Native API Reference

A consolidated summary of Bookvault's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://api.bookvault.app/v3/docs
- **OpenAPI specification:** https://api.bookvault.app/v3/swagger/docs/v3
- **API base URL:** `https://api.bookvault.app/v3`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.bookvault.app/api-setup)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (maximum 250). Use `page` in the query string to choose the page.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Address](actions/create-address.md) | `POST /Addresses` | [docs](https://api.bookvault.app/v3/docs#tag/Orders/operation/Addresses_post) |
| [Delete Address](actions/delete-address.md) | `DELETE /Addresses` | [docs](https://api.bookvault.app/v3/docs#tag/Orders/operation/Addresses_delete) |
| [Get Account](actions/get-account.md) | `GET /Account` | [docs](https://api.bookvault.app/v3/docs#tag/Account/operation/Account_Get) |
| [Get Ecologi Statistics](actions/get-ecologi-statistics.md) | `GET /Ecologi` | [docs](https://api.bookvault.app/v3/docs#tag/Enviromental/operation/Ecologi_get) |
| [List Address Groups](actions/list-address-groups.md) | `GET /AddressLists` | [docs](https://api.bookvault.app/v3/docs#tag/Addresses/operation/AddressLists_get) |
| [List Addresses](actions/list-addresses.md) | `GET /Addresses` | [docs](https://api.bookvault.app/v3/docs#tag/Orders/operation/Addresses_get) |
| [List Bindings](actions/list-bindings.md) | `GET /Bindings` | [docs](https://api.bookvault.app/v3/docs#tag/Titles/operation/Bindings_Get) |
| [List Collections](actions/list-collections.md) | `GET /Collections` | [docs](https://api.bookvault.app/v3/docs#tag/TGBBS/operation/Collections_Get) |
| [List Connected Apps](actions/list-connected-apps.md) | `GET /App` | [docs](https://api.bookvault.app/v3/docs#tag/Account/operation/App_Get) |
| [List Countries](actions/list-countries.md) | `GET /Countries` | [docs](https://api.bookvault.app/v3/docs#tag/Orders/operation/Countries_Get) |
| [List Imprints](actions/list-imprints.md) | `GET /Imprint` | [docs](https://api.bookvault.app/v3/docs#tag/Titles/operation/Imprint_Get) |
| [List IOSS Codes](actions/list-ioss-codes.md) | `GET /IOSS` | [docs](https://api.bookvault.app/v3/docs#tag/Account/operation/IOSS_Get) |
| [List Promo Codes](actions/list-promo-codes.md) | `GET /Promos` | [docs](https://api.bookvault.app/v3/docs#tag/TGBBS/operation/Promos_Get) |
| [List Publishers](actions/list-publishers.md) | `GET /Publisher` | [docs](https://api.bookvault.app/v3/docs#tag/Account/operation/Publisher_Get) |
| [List Reporting Types](actions/list-reporting-types.md) | `GET /ReportingTypes` | [docs](https://api.bookvault.app/v3/docs#tag/Reporting/operation/ReportingTypes_Get) |
| [List Retailers](actions/list-retailers.md) | `GET /Retailers` | [docs](https://api.bookvault.app/v3/docs#tag/Wholesale/operation/Retailers_Get) |
| [List Roles](actions/list-roles.md) | `GET /Roles` | [docs](https://api.bookvault.app/v3/docs#tag/Account/operation/Roles_get) |
| [List Sizes](actions/list-sizes.md) | `GET /Sizing` | [docs](https://api.bookvault.app/v3/docs#tag/Titles/operation/Sizing_Get) |
| [List Team Members](actions/list-team-members.md) | `GET /Team` | [docs](https://api.bookvault.app/v3/docs#tag/Account/operation/Team_get) |
| [Update Address](actions/update-address.md) | `PUT /Addresses` | [docs](https://api.bookvault.app/v3/docs#tag/Orders/operation/Addresses_put) |
