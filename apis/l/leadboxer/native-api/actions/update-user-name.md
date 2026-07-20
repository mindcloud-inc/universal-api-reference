# Update User Name with Leadboxer

Updates an existing user's name in Leadboxer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/users/{{userId}}/name`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Update User Name](https://developers.leadboxer.com/reference/updatename)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userId` | path | `number` | yes |
| `email` | query | `string` | yes |
| `firstName` | body | `string` | yes |
| `lastName` | body | `string` | yes |
