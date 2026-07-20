# Create Guest with Evenium

Creates a new guest in Evenium.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:eventId/guests`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Create Guest](https://static.evenium.com/api-docs/organizer/index-json.html#_create_guest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | Guest company. |
| `contactId` | body | `string` | no | Invite an existing contact by ID. |
| `email` | body | `string` | no | Guest email. |
| `eventId` | path | `string` | no | The Evenium event ID. |
| `firstName` | body | `string` | no | Guest first name. |
| `gender` | body | `string` | no | Guest gender. |
| `lastName` | body | `string` | no | Guest last name. |
| `status` | body | `string` | no | Guest registration status. |
