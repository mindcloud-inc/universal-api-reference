# timeBuzzer: Native API Reference

A consolidated summary of timeBuzzer's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://my.timebuzzer.com/doc/
- **API base URL:** `https://my.timebuzzer.com`

## Authentication

### API Key

Connect a timeBuzzer API key to read account, activity, tile, and webhook data.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documenter.getpostman.com/view/2798570/T17NbQjP)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `count` in the query string to set the page size (default 50). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST /open-api/activities` | [docs](https://my.timebuzzer.com/doc/#api-Activities-CreateActivity) |
| [Create Tile](actions/create-tile.md) | `POST /open-api/tiles` | [docs](https://my.timebuzzer.com/doc/#api-Tiles-CreateTile) |
| [Create Webhook Configuration](actions/create-webhook-configuration.md) | `POST /open-api/webhooks` | [docs](https://my.timebuzzer.com/doc/#api-Webhook-SaveNewWebhooks) |
| [Delete Activity](actions/delete-activity.md) | `DELETE /open-api/activities/:id` | [docs](https://my.timebuzzer.com/doc/#api-Activities-DeleteActivity) |
| [Delete Webhook Configuration](actions/delete-webhook-configuration.md) | `DELETE /open-api/webhooks/:id` | [docs](https://my.timebuzzer.com/doc/) |
| [Delete Webhook Configuration By URL](actions/delete-webhook-configuration-by-url.md) | `DELETE /open-api/webhooks` | [docs](https://my.timebuzzer.com/doc/) |
| [Get My Account](actions/get-my-account.md) | `GET /open-api/account/me` | [docs](https://my.timebuzzer.com/doc/#api-Account-GetMyAccount) |
| [Get Tile](actions/get-tile.md) | `GET /open-api/tiles/:id` | [docs](https://my.timebuzzer.com/doc/#api-Tiles-GetTileById) |
| [List Activities](actions/list-activities.md) | `GET /open-api/activities` | [docs](https://my.timebuzzer.com/doc/#api-Activities-GetAllActivities) |
| [List Layers](actions/list-layers.md) | `GET /open-api/layers` | [docs](https://my.timebuzzer.com/doc/#api-Layers-GetAllLayers) |
| [List Tiles](actions/list-tiles.md) | `GET /open-api/tiles` | [docs](https://my.timebuzzer.com/doc/#api-Tiles-GetAllTiles) |
| [List Webhook Configurations](actions/list-webhook-configurations.md) | `GET /open-api/webhooks` | [docs](https://my.timebuzzer.com/doc/#api-Webhook-LoadWebhooks) |
| [Search Activities](actions/search-activities.md) | `POST /open-api/activities/filters` | [docs](https://my.timebuzzer.com/doc/#api-Activities-GetFilteredActivities) |
| [Search Tiles](actions/search-tiles.md) | `POST /open-api/tiles/filters` | [docs](https://my.timebuzzer.com/doc/#api-Tiles-GetFilteredTiles) |
| [Update Activity](actions/update-activity.md) | `PUT /open-api/activities/:id` | [docs](https://my.timebuzzer.com/doc/#api-Activities-EditActivity) |
| [Update Tile](actions/update-tile.md) | `PUT /open-api/tiles/:id` | [docs](https://my.timebuzzer.com/doc/#api-Tiles-EditTile) |
| [Update Webhook Configuration](actions/update-webhook-configuration.md) | `PUT /open-api/webhooks/:id` | [docs](https://my.timebuzzer.com/doc/#api-Webhook-SaveWebhooks) |
