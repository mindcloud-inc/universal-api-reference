# Update User with 123FormBuild

Updates an existing user in 123FormBuilder.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/{identifier}`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Update User](https://www.123formbuilder.com/developer/api-v2-users/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The identifier of the user to update |
| `email` | body | `string` | no | Email for the user |
| `password` | body | `string` | no | Password for the user |
| `passhash` | body | `string` | no | Hashed password for the user |
| `admin` | body | `number` | no | Admin flag for the user |
| `company_name` | body | `string` | no | Company name for the user |
| `allow_create_form` | body | `number` | no | Permission to create forms |
| `allow_duplicate_form` | body | `number` | no | Permission to duplicate forms |
| `allow_delete_form` | body | `number` | no | Permission to delete forms |
| `can_manage_groups` | body | `number` | no | Permission to manage groups |
| `can_manage_users` | body | `number` | no | Permission to manage users |
