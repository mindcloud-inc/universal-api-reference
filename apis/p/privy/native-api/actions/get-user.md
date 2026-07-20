# Get User with Privy

Retrieves a user from Privy by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/{{userId}}`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Get User](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1{user_id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | Privy user ID. This normally starts with did:privy:. |
