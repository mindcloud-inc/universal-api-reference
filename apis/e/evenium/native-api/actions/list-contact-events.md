# List Contact Events with Evenium

Retrieves a contact's events from Evenium.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contactId/events`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [List Contact Events](https://static.evenium.com/api-docs/organizer/index-json.html#_get_contacts_events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | The Evenium Contact ID. |
