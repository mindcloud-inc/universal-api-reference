# Create a new role with Digital Samba

Creates a new role in Digital Samba.

## Endpoint

- **Method:** `POST`
- **Path:** `/roles`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Create a new role](https://developer.digitalsamba.com/rest-api/#roles-POSTapi-v1-roles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | JSON request body documented for this endpoint. |
| `name` | body | `string` | yes | Must contain only letters, numbers, dashes and underscores. Must not be greater than 30 characters. Must be unique. |
| `display_name` | body | `string` | yes | Must be at least 3 characters. Must not be greater than 100 characters. |
| `description` | body | `string` | no | — |
| `permissions` | body | `object` | yes | Must be an array of permissions. |
