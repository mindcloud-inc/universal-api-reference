# Seam: Native API Reference

A consolidated summary of Seam's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.seam.co/latest
- **OpenAPI specification:** https://connect.getseam.com/openapi.json
- **API base URL:** `https://connect.getseam.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.seam.co/latest/core-concepts/authentication/api-keys)

## API conventions

The next-page cursor is read from `pagination.nextPageCursor`.

## Pagination

Use `limit` in the request body to set the page size. Use `page_cursor` in the request body as the pagination cursor.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Connect Webview](actions/create-connect-webview.md) | `POST /connect_webviews/create` | [docs](https://docs.seam.co/latest/api/connect_webviews/create) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/create` | [docs](https://docs.seam.co/latest/api/webhooks/create) |
| [Delete Webhook](actions/delete-webhook.md) | `POST /webhooks/delete` | [docs](https://docs.seam.co/latest/api/webhooks/delete) |
| [Get Connect Webview](actions/get-connect-webview.md) | `POST /connect_webviews/get` | [docs](https://docs.seam.co/latest/api/connect_webviews/get) |
| [Get Connected Account](actions/get-connected-account.md) | `POST /connected_accounts/get` | [docs](https://docs.seam.co/latest/api/connected_accounts/get) |
| [Get Device](actions/get-device.md) | `POST /devices/get` | [docs](https://docs.seam.co/latest/api/devices/get) |
| [Get Event](actions/get-event.md) | `POST /events/get` | [docs](https://docs.seam.co/latest/api/events/get) |
| [Get Lock](actions/get-lock.md) | `POST /locks/get` | [docs](https://docs.seam.co/latest/api/locks/get) |
| [Get Thermostat](actions/get-thermostat.md) | `POST /thermostats/get` | [docs](https://docs.seam.co/latest/api/thermostats/get) |
| [Get Webhook](actions/get-webhook.md) | `POST /webhooks/get` | [docs](https://docs.seam.co/latest/api/webhooks/get) |
| [Get Workspace](actions/get-workspace.md) | `POST /workspaces/get` | [docs](https://docs.seam.co/latest/api/workspaces/get) |
| [List Connect Webviews](actions/list-connect-webviews.md) | `POST /connect_webviews/list` | [docs](https://docs.seam.co/latest/api/connect_webviews/list) |
| [List Connected Accounts](actions/list-connected-accounts.md) | `POST /connected_accounts/list` | [docs](https://docs.seam.co/latest/api/connected_accounts/list) |
| [List Device Providers](actions/list-device-providers.md) | `POST /devices/list_device_providers` | [docs](https://docs.seam.co/latest/api/devices/list_device_providers) |
| [List Devices](actions/list-devices.md) | `POST /devices/list` | [docs](https://docs.seam.co/latest/api/devices/list) |
| [List Events](actions/list-events.md) | `POST /events/list` | [docs](https://docs.seam.co/latest/api/events/list) |
| [List Locks](actions/list-locks.md) | `POST /locks/list` | [docs](https://docs.seam.co/latest/api/locks/list) |
| [List Noise Sensors](actions/list-noise-sensors.md) | `POST /noise_sensors/list` | [docs](https://docs.seam.co/latest/api/noise_sensors/list) |
| [List Phones](actions/list-phones.md) | `POST /phones/list` | [docs](https://docs.seam.co/latest/api/phones/list) |
| [List Thermostats](actions/list-thermostats.md) | `POST /thermostats/list` | [docs](https://docs.seam.co/latest/api/thermostats/list) |
| [List Webhooks](actions/list-webhooks.md) | `POST /webhooks/list` | [docs](https://docs.seam.co/latest/api/webhooks/list) |
| [List Workspaces](actions/list-workspaces.md) | `POST /workspaces/list` | [docs](https://docs.seam.co/latest/api/workspaces/list) |
| [Update Webhook](actions/update-webhook.md) | `POST /webhooks/update` | [docs](https://docs.seam.co/latest/api/webhooks/update) |
