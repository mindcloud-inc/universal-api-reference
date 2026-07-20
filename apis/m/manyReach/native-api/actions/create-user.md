# Create User with ManyReach

Creates a new user in ManyReach.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.manyreach.com/api/v2/users`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Create User](https://api.manyreach.com/api#v2/tag/user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountType` | body | `string` | yes | User permission level. |
| `email` | body | `string` | yes | User email address. |
| `firstName` | body | `string` | no | User first name. |
| `lastName` | body | `string` | no | User last name. |
