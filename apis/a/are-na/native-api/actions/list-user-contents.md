# List User Contents with Are.na

Retrieves contents created by a user in Are.na.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:id/contents`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [List User Contents](https://www.are.na/developers/explore/user/contents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Are.na user ID or slug. |
