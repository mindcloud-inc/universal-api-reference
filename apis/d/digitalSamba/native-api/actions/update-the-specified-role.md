# Update the specified role with Digital Samba

Updates an existing role in Digital Samba.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/roles/:role`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Update the specified role](https://developer.digitalsamba.com/rest-api/#roles-PATCHapi-v1-roles--role-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `role` | path | `string` | yes | Role path parameter. |
| `body` | body | `object` | no | JSON request body documented for this endpoint. |
| `name` | body | `string` | no | Must contain only letters, numbers, dashes and underscores. Must not be greater than 30 characters. Must be unique. |
| `display_name` | body | `string` | no | Must be at least 3 characters. Must not be greater than 100 characters. |
| `description` | body | `string` | no | — |
| `permissions` | body | `object` | yes | Must be an array of permissions. |
