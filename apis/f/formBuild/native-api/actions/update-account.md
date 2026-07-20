# Update Account with 123FormBuild

Updates an existing account in 123FormBuilder.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/{user_id}`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Update Account](https://www.123formbuilder.com/developer/api-v2/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user account |
| `email` | body | `string` | yes | Email for the account |
| `password` | body | `string` | yes | Password for the account |
| `password_repeat` | body | `string` | yes | Repeated password for confirmation |
| `plan` | body | `string` | no | Plan for the account |
| `company_name` | body | `string` | no | Company name for the account |
