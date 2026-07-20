# Create List with SureContact

Creates a new list in SureContact.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/public/lists`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Create List](https://api.surecontact.com/docs#list-management-POSTapi-v1-public-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional description for the list. |
| `filters` | body | `object` | no | Filter criteria for dynamic lists. |
| `name` | body | `string` | yes | The name of the list. |
| `type` | body | `string` | no | The list type: static or dynamic. |
