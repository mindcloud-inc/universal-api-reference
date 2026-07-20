# <img src="https://images.mindcloud.co/apps/icons/livekit-color_1776188816692.png" alt="LiveKit logo" width="28" height="28"> LiveKit: Universal API

LiveKit is an open source platform for realtime audio, video, telephony, and AI agent communications.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/liveKit/latest
- **Category:** Communication / Video Communications
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://livekit.io
- **Vendor API docs:** https://docs.livekit.io/reference/server/server-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Rooms](actions/list-rooms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveKit/latest/actions/list-rooms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Attendees

| Action | Method | Description |
| --- | --- | --- |
| [List Participants](actions/list-participants.md) | GET | Retrieves participants in a LiveKit room. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Create Ingress](actions/create-ingress.md) | POST | Creates a new ingress in LiveKit. |
| [Delete Ingress](actions/delete-ingress.md) | DELETE | Deletes an existing ingress from LiveKit. |
| [List Ingresses](actions/list-ingresses.md) | GET | Retrieves ingresses from LiveKit. |
| [Update Ingress](actions/update-ingress.md) | PUT | Updates an existing ingress in LiveKit. |

### Meetings

| Action | Method | Description |
| --- | --- | --- |
| [Create Room](actions/create-room.md) | POST | Creates a new room in LiveKit. |
| [Delete Room](actions/delete-room.md) | DELETE | Deletes an existing room from LiveKit. |
| [List Rooms](actions/list-rooms.md) | GET | Retrieves rooms from LiveKit. |
| [Update Room Metadata](actions/update-room-metadata.md) | PUT | Updates metadata for an existing LiveKit room. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Send Data](actions/send-data.md) | POST | Sends data to participants in a LiveKit room. |

