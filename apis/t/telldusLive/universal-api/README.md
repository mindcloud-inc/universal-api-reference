# <img src="https://images.mindcloud.co/apps/icons/telldus-logo-primary-black_1776821091703.png" alt="Telldus Live! logo" width="28" height="28"> Telldus Live!: Universal API

Control devices and monitor sensors with Telldus Live!

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/telldusLive/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://telldus.com/en/pages/telldus-live
- **Vendor API docs:** https://developer.telldus.com/wiki/Guides/Telldus%20Live%20API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Clients](actions/list-clients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telldusLive/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | GET | Retrieves your clients from Telldus Live!. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Retrieves your devices from Telldus Live!. |
| [List Events](actions/list-events.md) | GET | Retrieves your events from Telldus Live!. |
| [List Modes](actions/list-modes.md) | GET | Retrieves your modes from Telldus Live!. |
| [List Rooms](actions/list-rooms.md) | GET | Retrieves your rooms from Telldus Live!. |
| [List Sensors](actions/list-sensors.md) | GET | Retrieves your sensors from Telldus Live!. |

