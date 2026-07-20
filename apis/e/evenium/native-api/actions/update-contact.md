# Update Contact with Evenium

Updates an existing contact in Evenium.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contactId`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Update Contact](https://static.evenium.com/api-docs/organizer/index-json.html#_update_contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | The Evenium Company. |
| `contactId` | path | `number` | yes | The Evenium Contact ID. |
| `email` | body | `string` | no | The Evenium Email. |
