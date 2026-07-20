# Import Guests with Evenium

Imports guests into Evenium.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:eventId/guests`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Import Guests](https://static.evenium.com/api-docs/organizer/index-json.html#_import_guests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | no | The Evenium event ID. |
| `guests` | body | `string` | no | Guests payload for bulk import. |
| `mode` | query | `string` | no | Import mode. |
