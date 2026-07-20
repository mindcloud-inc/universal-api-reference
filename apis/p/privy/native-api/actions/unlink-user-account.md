# Unlink User Account with Privy

Unlinks a linked account from a Privy user.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/{{userId}}/accounts/unlink`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Unlink User Account](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1{user_id}~1accounts~1unlink/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | Privy user ID. This normally starts with did:privy:. |
