# <img src="https://images.mindcloud.co/apps/icons/favicon-shop-lightwaverf-com-48x48_1776436438014.png" alt="LightwaveRF Lighting logo" width="28" height="28"> LightwaveRF Lighting: Universal API

Control and manage LightwaveRF Smart Series structures, zones, rooms, favourites, features, devices, historical data, and webhooks through the Link Plus Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lightwaveRFLighting/latest
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shop.lightwaverf.com/
- **Vendor API docs:** https://support.lightwaverf.com/knowledge/link-plus-smart-series-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFLighting/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Add Device](actions/add-device.md) | POST | Adds a device to LightwaveRF Lighting. |
| [Add LinkPlus](actions/add-link-plus.md) | POST | Adds a Link Plus to LightwaveRF Lighting. |
| [Batch Read Features](actions/batch-read-features.md) | GET | Retrieves multiple features from LightwaveRF Lighting. |
| [Batch Read Historical Data](actions/batch-read-historical-data.md) | GET | Retrieves historical data for multiple features from LightwaveRF Lighting. |
| [Batch Write Features](actions/batch-write-features.md) | PUT | Updates multiple features in LightwaveRF Lighting. |
| [Delete Device](actions/delete-device.md) | DELETE | Deletes an existing device from LightwaveRF Lighting. |
| [Get Feature](actions/get-feature.md) | GET | Retrieves a feature value from LightwaveRF Lighting. |
| [Read Historical Data](actions/read-historical-data.md) | GET | Retrieves historical data from LightwaveRF Lighting. |
| [Set Feature](actions/set-feature.md) | PUT | Updates a feature value in LightwaveRF Lighting. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Room](actions/create-room.md) | POST | Creates a new room in LightwaveRF Lighting. |
| [Create Zone](actions/create-zone.md) | POST | Creates a new zone in LightwaveRF Lighting. |
| [Delete Room](actions/delete-room.md) | DELETE | Deletes an existing room from LightwaveRF Lighting. |
| [Delete Zone](actions/delete-zone.md) | DELETE | Deletes an existing zone from LightwaveRF Lighting. |
| [Get Favourite](actions/get-favourite.md) | GET | Retrieves a favourite from LightwaveRF Lighting. |
| [Get Room](actions/get-room.md) | GET | Retrieves a room from LightwaveRF Lighting. |
| [Get Structure](actions/get-structure.md) | GET | Retrieves a structure from LightwaveRF Lighting. |
| [Get Zone](actions/get-zone.md) | GET | Retrieves a zone from LightwaveRF Lighting. |
| [List Favourites](actions/list-favourites.md) | GET | Retrieves configured favourites from LightwaveRF Lighting. |
| [List Hierarchy](actions/list-hierarchy.md) | GET | Retrieves hierarchy data from LightwaveRF Lighting. |
| [List Rooms](actions/list-rooms.md) | GET | Retrieves available rooms from LightwaveRF Lighting. |
| [List Structures](actions/list-structures.md) | GET | Retrieves available structures from LightwaveRF Lighting. |
| [List Zones](actions/list-zones.md) | GET | Retrieves available zones from LightwaveRF Lighting. |
| [Update Favourite](actions/update-favourite.md) | PUT | Updates an existing favourite in LightwaveRF Lighting. |
| [Update Room](actions/update-room.md) | PUT | Updates an existing room in LightwaveRF Lighting. |
| [Update Zone](actions/update-zone.md) | PUT | Updates an existing zone in LightwaveRF Lighting. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves user information from LightwaveRF Lighting. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in LightwaveRF Lighting. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from LightwaveRF Lighting. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from LightwaveRF Lighting. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves configured webhooks from LightwaveRF Lighting. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in LightwaveRF Lighting. |

