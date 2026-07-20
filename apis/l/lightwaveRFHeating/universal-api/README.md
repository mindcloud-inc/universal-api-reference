# <img src="https://images.mindcloud.co/apps/icons/favicon-lightwaverf-com-48x48_1777315463024.png" alt="LightwaveRF Heating logo" width="28" height="28"> LightwaveRF Heating: Universal API

Control and inspect LightwaveRF Smart Series heating context, rooms, features, feature writes, and historical data through the Link Plus Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lightwaveRFHeating/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lightwaverf.com
- **Vendor API docs:** https://support.lightwaverf.com/knowledge/link-plus-smart-series-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFHeating/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Batch Read Heating Features](actions/batch-read-heating-features.md) | GET | Retrieves multiple heating features from LightwaveRF Heating. |
| [Batch Read Heating Historical Data](actions/batch-read-heating-historical-data.md) | GET | Retrieves historical heating data from LightwaveRF Heating in batch. |
| [Batch Write Heating Features](actions/batch-write-heating-features.md) | PUT | Updates multiple heating features in LightwaveRF Heating. |
| [Get Heating Feature](actions/get-heating-feature.md) | GET | Retrieves a heating feature from LightwaveRF Heating. |
| [Read Heating Historical Data](actions/read-heating-historical-data.md) | GET | Retrieves historical heating data from LightwaveRF Heating. |
| [Set Heating Feature](actions/set-heating-feature.md) | PUT | Updates an existing heating feature in LightwaveRF Heating. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Room](actions/get-room.md) | GET | Retrieves a room from LightwaveRF Heating. |
| [Get Structure](actions/get-structure.md) | GET | Retrieves a structure from LightwaveRF Heating. |
| [List Heating Hierarchy](actions/list-heating-hierarchy.md) | GET | Retrieves the heating hierarchy from LightwaveRF Heating. |
| [List Rooms](actions/list-rooms.md) | GET | Retrieves account rooms from LightwaveRF Heating. |
| [List Structures](actions/list-structures.md) | GET | Retrieves account structures from LightwaveRF Heating. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves the current user's account details from LightwaveRF Heating. |

