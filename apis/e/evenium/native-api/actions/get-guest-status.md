# Get Guest Status with Evenium

Retrieves a guest status from Evenium.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/guests/:contactId/status`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Get Guest Status](https://static.evenium.com/api-docs/organizer/index-json.html#_get_guest_status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | The Evenium Contact ID. |
| `eventId` | path | `number` | yes | The Evenium Event ID. |
