# Get Guest with Evenium

Retrieves a guest from Evenium.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/guests/:contactId`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Get Guest](https://static.evenium.com/api-docs/organizer/index-json.html#_get_guest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | The Evenium Contact ID. |
| `eventId` | path | `number` | yes | The Evenium Event ID. |
