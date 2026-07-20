# <img src="https://images.mindcloud.co/apps/icons/favicon-lightwaverf-com-48x48_1777315559811.png" alt="LightwaveRF Power logo" width="28" height="28"> LightwaveRF Power: Universal API

Control and manage LightwaveRF Smart Series power devices, structures, rooms, zones, favourites, feature values, device pairing, and historical data through the Link Plus Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lightwaveRFPower/latest
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lightwaverf.com
- **Vendor API docs:** https://support.lightwaverf.com/knowledge/link-plus-smart-series-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Structures](actions/list-structures.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/list-structures?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Add Device](actions/add-device.md) | POST | Creates a new device in LightwaveRF Power. |
| [Add LinkPlus](actions/add-link-plus.md) | POST | Adds a Link Plus device in LightwaveRF Power. |
| [Batch Read Features](actions/batch-read-features.md) | GET | Retrieves multiple features from LightwaveRF Power. |
| [Batch Read Historical Data](actions/batch-read-historical-data.md) | GET | Retrieves historical data for multiple devices in LightwaveRF Power. |
| [Batch Write Features](actions/batch-write-features.md) | PUT | Updates multiple features in LightwaveRF Power. |
| [Delete Device](actions/delete-device.md) | DELETE | Deletes an existing device from LightwaveRF Power. |
| [Get Feature](actions/get-feature.md) | GET | Retrieves a feature from LightwaveRF Power. |
| [Read Historical Data](actions/read-historical-data.md) | GET | Retrieves historical data from LightwaveRF Power. |
| [Set Feature](actions/set-feature.md) | PUT | Updates a feature in LightwaveRF Power. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Room](actions/create-room.md) | POST | Creates a new room in LightwaveRF Power. |
| [Create Zone](actions/create-zone.md) | POST | Creates a new zone in LightwaveRF Power. |
| [Delete Room](actions/delete-room.md) | DELETE | Deletes an existing room from LightwaveRF Power. |
| [Delete Zone](actions/delete-zone.md) | DELETE | Deletes an existing zone from LightwaveRF Power. |
| [Get Favourite](actions/get-favourite.md) | GET | Retrieves a favourite from LightwaveRF Power. |
| [Get Room](actions/get-room.md) | GET | Retrieves a room from LightwaveRF Power. |
| [Get Structure](actions/get-structure.md) | GET | Retrieves a structure from LightwaveRF Power. |
| [Get Zone](actions/get-zone.md) | GET | Retrieves a zone from LightwaveRF Power. |
| [List Favourites](actions/list-favourites.md) | GET | Retrieves favourites from LightwaveRF Power. |
| [List Hierarchy](actions/list-hierarchy.md) | GET | Retrieves the structure hierarchy from LightwaveRF Power. |
| [List Rooms](actions/list-rooms.md) | GET | Retrieves rooms from LightwaveRF Power. |
| [List Structures](actions/list-structures.md) | GET | Retrieves structures from LightwaveRF Power. |
| [List Zones](actions/list-zones.md) | GET | Retrieves zones from LightwaveRF Power. |
| [Update Favourite](actions/update-favourite.md) | PUT | Updates an existing favourite in LightwaveRF Power. |
| [Update Room](actions/update-room.md) | PUT | Updates an existing room in LightwaveRF Power. |
| [Update Zone](actions/update-zone.md) | PUT | Updates an existing zone in LightwaveRF Power. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves user info from LightwaveRF Power. |

