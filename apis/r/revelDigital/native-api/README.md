# Revel Digital: Native API Reference

A consolidated summary of Revel Digital's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.reveldigital.com/rest-api/
- **OpenAPI specification:** https://api.reveldigital.com/swagger/v1/swagger.json
- **API base URL:** `https://api.reveldigital.com`

## Authentication

### API Key

Use a Revel Digital developer API key from your account settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-RevelDigital-ApiKey: <apiKey>
```

[Official authentication documentation](https://support.reveldigital.com/hc/en-us/articles/360061984171-Zapier-Integration)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Data Table](actions/create-data-table.md) | `POST /datatables` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Create Data Table Row](actions/create-data-table-row.md) | `POST /datatables/:tableId/rows` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Delete Data Table Row](actions/delete-data-table-row.md) | `DELETE /datatables/:tableId/rows/:rowId` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Get Account Details](actions/get-account-details.md) | `GET /account` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Get Alert](actions/get-alert.md) | `GET /alerts/:id` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Get Audit Event](actions/get-audit-event.md) | `GET /account/auditevents/:eventId` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Get Data Table](actions/get-data-table.md) | `GET /datatables/:tableId` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Get Data Table Row](actions/get-data-table-row.md) | `GET /datatables/:tableId/rows/:rowId` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Get Device](actions/get-device.md) | `GET /devices/:id` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Get Media Item](actions/get-media-item.md) | `GET /media/:id` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Get Playlist](actions/get-playlist.md) | `GET /playlists/:id` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Get Schedule](actions/get-schedule.md) | `GET /schedules/:id` | [docs](https://developer.reveldigital.com/rest-api/) |
| [List Alerts](actions/list-alerts.md) | `GET /alerts` | [docs](https://developer.reveldigital.com/rest-api/) |
| [List Audit Events](actions/list-audit-events.md) | `GET /account/auditevents` | [docs](https://developer.reveldigital.com/rest-api/) |
| [List Data Table Rows](actions/list-data-table-rows.md) | `GET /datatables/:tableId/rows` | [docs](https://developer.reveldigital.com/rest-api/) |
| [List Data Tables](actions/list-data-tables.md) | `GET /datatables` | [docs](https://developer.reveldigital.com/rest-api/) |
| [List Device Groups](actions/list-device-groups.md) | `GET /devices/groups` | [docs](https://developer.reveldigital.com/rest-api/) |
| [List Devices](actions/list-devices.md) | `GET /devices` | [docs](https://developer.reveldigital.com/rest-api/) |
| [List Media](actions/list-media.md) | `GET /media` | [docs](https://developer.reveldigital.com/rest-api/) |
| [List Organizations](actions/list-organizations.md) | `GET /account/organizations` | [docs](https://developer.reveldigital.com/rest-api/) |
| [List Playlists](actions/list-playlists.md) | `GET /playlists` | [docs](https://developer.reveldigital.com/rest-api/) |
| [List Schedules](actions/list-schedules.md) | `GET /schedules` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Replace Playlist](actions/replace-playlist.md) | `PUT /playlists/:id` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Send Commands to Multiple Devices](actions/send-commands-to-multiple-devices.md) | `POST /devices/commands` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Update Account](actions/update-account.md) | `PUT /account` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Update Alert](actions/update-alert.md) | `PUT /alerts/:id` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Update Data Table](actions/update-data-table.md) | `PUT /datatables/:tableId` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Update Data Table Row](actions/update-data-table-row.md) | `PUT /datatables/:tableId/rows/:rowId` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Update Device](actions/update-device.md) | `PUT /devices/:id` | [docs](https://developer.reveldigital.com/rest-api/) |
| [Update Media Item](actions/update-media-item.md) | `PUT /media/:id` | [docs](https://developer.reveldigital.com/rest-api/) |
