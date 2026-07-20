# Update Guest with Evenium

Updates an existing guest in Evenium.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:eventId/guests/:contactId`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Update Guest](https://static.evenium.com/api-docs/organizer/index-json.html#_update_guest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | Guest company. |
| `contactId` | path | `string` | no | The Evenium contact ID. |
| `email` | body | `string` | no | Guest email. |
| `eventId` | path | `string` | no | The Evenium event ID. |
| `status` | body | `string` | no | Guest registration status. |
