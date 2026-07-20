# Set User Custom Metadata with Privy

Updates custom metadata for a user in Privy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/users/{{userId}}/custom_metadata`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Set User Custom Metadata](https://api.privy.io/v1/openapi.json#/paths/~1v1~1users~1{user_id}~1custom_metadata/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | Privy user ID. This normally starts with did:privy:. |
