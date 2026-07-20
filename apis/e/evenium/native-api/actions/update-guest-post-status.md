# Update Guest Post Status with Evenium

Updates a guest post status in Evenium.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:eventId/guests/:contactId/postStatus`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Update Guest Post Status](https://static.evenium.com/api-docs/organizer/index-json.html#_update_guest_post_status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | no | The Evenium contact ID. |
| `eventId` | path | `string` | no | The Evenium event ID. |
| `lastUpdate` | body | `string` | no | The date the status was updated. |
| `value` | body | `string` | no | The new guest post status. |
