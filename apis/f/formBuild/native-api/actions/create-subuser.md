# Create Subuser with 123FormBuild

Creates a new subuser in 123FormBuilder.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Create Subuser](https://www.123formbuilder.com/developer/api-v2-users/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Email for the new subuser |
| `name` | body | `string` | no | Name of the new subuser |
| `password` | body | `string` | no | Password for the new subuser |
| `passhash` | body | `string` | no | Hashed password for the new subuser |
| `admin` | body | `number` | no | Admin flag for the subuser |
| `company_name` | body | `string` | no | Company name for the subuser |
| `allow_create_form` | body | `number` | no | Permission to create forms |
| `allow_duplicate_form` | body | `number` | no | Permission to duplicate forms |
| `allow_delete_form` | body | `number` | no | Permission to delete forms |
| `can_manage_groups` | body | `number` | no | Permission to manage groups |
| `can_manage_users` | body | `number` | no | Permission to manage users |
