# Update user with Statsig

Updates a user in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/users/{email}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update user](https://docs.statsig.com/api-reference/users/update-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | email |
| `role` | body | `string` | no | Request body field. |
| `firstName` | body | `string` | no | Request body field. |
| `lastName` | body | `string` | no | Request body field. |
