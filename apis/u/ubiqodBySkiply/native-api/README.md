# Ubiqod by Skiply: Native API Reference

A consolidated summary of Ubiqod by Skiply's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/connectors/ubiqodbyskiply/
- **OpenAPI specification:** https://raw.githubusercontent.com/microsoft/PowerPlatformConnectors/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)/apiDefinition.swagger.json
- **API base URL:** `https://api.ubiqod.com`

## Authentication

### API Key

Authenticate Ubiqod API requests with an API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.skiply.eu/en/docs/where-can-i-find-my-ubiqod-api-keys/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Badges To Badge List](actions/add-badges-to-badge-list.md) | `POST /badges/:badgeListId/codes` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Add Codes To PIN Code List](actions/add-codes-to-pin-code-list.md) | `POST /pincodes/:pinCodeListId/codes` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Create Badge List](actions/create-badge-list.md) | `POST /badges/` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Create PIN Code List](actions/create-pin-code-list.md) | `POST /pincodes/` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Create QR Code Tracker](actions/create-qr-code-tracker.md) | `POST /trackers/` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Create Site](actions/create-site.md) | `POST /sites/` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Delete Badge List](actions/delete-badge-list.md) | `DELETE /badges/:badgeListId` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Delete Badges From Badge List](actions/delete-badges-from-badge-list.md) | `DELETE /badges/:badgeListId/codes` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Delete Codes From PIN Code List](actions/delete-codes-from-pin-code-list.md) | `DELETE /pincodes/:pinCodeListId/codes` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Delete PIN Code List](actions/delete-pin-code-list.md) | `DELETE /pincodes/:pinCodeListId` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Delete Site](actions/delete-site.md) | `DELETE /sites/:siteId` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Delete Tracker](actions/delete-tracker.md) | `DELETE /trackers/:trackerSlug` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Get PIN Code List](actions/get-pin-code-list.md) | `GET /pincodes/:pinCodeListId` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Get Site](actions/get-site.md) | `GET /sites/:siteId` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Get Tracker](actions/get-tracker.md) | `GET /trackers/:trackerSlug` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [List Automation Dispatches](actions/list-automation-dispatches.md) | `GET /dispatchs/` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [List Badge Lists](actions/list-badge-lists.md) | `GET /badges/` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [List Interfaces](actions/list-interfaces.md) | `GET /interfaces` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [List PIN Code Lists](actions/list-pin-code-lists.md) | `GET /pincodes/` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [List Sites](actions/list-sites.md) | `GET /sites/` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [List Trackers](actions/list-trackers.md) | `GET /trackers/` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Update Badge List](actions/update-badge-list.md) | `PATCH /badges/:badgeListId` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Update Badges In Badge List](actions/update-badges-in-badge-list.md) | `PATCH /badges/:badgeListId/codes` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Update Codes In PIN Code List](actions/update-codes-in-pin-code-list.md) | `PATCH /pincodes/:pinCodeListId/codes` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Update PIN Code List](actions/update-pin-code-list.md) | `PATCH /pincodes/:pinCodeListId` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Update Site](actions/update-site.md) | `PATCH /sites/:siteId` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
| [Update Tracker](actions/update-tracker.md) | `PATCH /trackers/:trackerSlug` | [docs](https://github.com/microsoft/PowerPlatformConnectors/tree/dev/certified-connectors/Ubiqod%20by%20Skiply%20(v2)) |
