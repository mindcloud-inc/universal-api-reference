# Update Contact by Custom ID with Evenium

Updates a contact in Evenium by custom ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/customId/:customId`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Update Contact by Custom ID](https://static.evenium.com/api-docs/organizer/index-json.html#_update_contact_by_custom_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | The Evenium Company. |
| `customId` | path | `string` | yes | The Evenium Custom ID. |
| `email` | body | `string` | no | The Evenium Email. |
