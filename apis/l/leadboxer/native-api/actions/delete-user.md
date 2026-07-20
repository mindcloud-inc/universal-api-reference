# Delete User with Leadboxer

Deletes an existing user from Leadboxer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/users/{{userId}}`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Delete User](https://developers.leadboxer.com/reference/removeuser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userId` | path | `number` | yes |
| `email` | query | `string` | yes |
