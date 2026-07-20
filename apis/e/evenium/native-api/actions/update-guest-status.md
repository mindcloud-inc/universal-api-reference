# Update Guest Status with Evenium

Updates a guest status in Evenium.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:eventId/guests/:contactId/status`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Update Guest Status](https://static.evenium.com/api-docs/organizer/index-json.html#_update_guest_status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | no | The Evenium contact ID. |
| `eventId` | path | `string` | no | The Evenium event ID. |
| `status` | body | `string` | no | The new guest status. |
