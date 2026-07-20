# List Guest Accommodations with Evenium

Retrieves guest accommodations from Evenium.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/guests/:contactId/accommodations`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [List Guest Accommodations](https://static.evenium.com/api-docs/organizer/index-json.html#_get_guest_accommodations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | The Evenium Contact ID. |
| `eventId` | path | `number` | yes | The Evenium Event ID. |
