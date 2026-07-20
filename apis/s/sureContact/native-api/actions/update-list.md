# Update List with SureContact

Updates an existing list in SureContact.

## Endpoint

- **Method:** `PUT`
- **Path:** `api/v1/public/lists/:list_uuid`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Update List](https://api.surecontact.com/docs#list-management-PUTapi-v1-public-lists--list_uuid-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional description for the list. |
| `filters` | body | `object` | no | Filter criteria for dynamic lists. |
| `list_uuid` | path | `string` | yes | The UUID of the list. |
| `name` | body | `string` | no | The name of the list. |
| `type` | body | `string` | no | The list type: static or dynamic. |
