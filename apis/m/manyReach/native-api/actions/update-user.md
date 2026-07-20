# Update User with ManyReach

Updates an existing user in ManyReach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.manyreach.com/api/v2/users/:id`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Update User](https://api.manyreach.com/api#v2/tag/user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountType` | body | `string` | no | User permission level. |
| `firstName` | body | `string` | no | User first name. |
| `id` | path | `string` | yes | The ID of the user to update. |
| `lastName` | body | `string` | no | User last name. |
