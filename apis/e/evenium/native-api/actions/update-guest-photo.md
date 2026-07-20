# Update Guest Photo with Evenium

Updates a guest photo in Evenium.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:eventId/guests/:contactId/photo`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Update Guest Photo](https://static.evenium.com/api-docs/organizer/index-json.html#_update_guest_photo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | no | The Evenium contact ID. |
| `eventId` | path | `string` | no | The Evenium event ID. |
| `photoDataUri` | body | `string` | no | Image encoded as a data URI. |
