# Get Guest Post Status with Evenium

Retrieves a guest post status from Evenium.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/guests/:contactId/postStatus`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Get Guest Post Status](https://static.evenium.com/api-docs/organizer/index-json.html#_get_guest_post_status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | The Evenium Contact ID. |
| `eventId` | path | `number` | yes | The Evenium Event ID. |
