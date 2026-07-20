# List Contact Events by Custom ID with Evenium

Retrieves a contact's events from Evenium by custom ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/customId/:customId/events`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [List Contact Events by Custom ID](https://static.evenium.com/api-docs/organizer/index-json.html#_get_contacts_events_by_custom_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customId` | path | `string` | no | The Evenium Custom ID. |
