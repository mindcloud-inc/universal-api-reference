# Create User Embedded Wallet with Privy

Creates an embedded wallet for a Privy user.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/{{userId}}/wallets`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Create User Embedded Wallet](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1{user_id}~1wallets/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | Privy user ID. This normally starts with did:privy:. |
