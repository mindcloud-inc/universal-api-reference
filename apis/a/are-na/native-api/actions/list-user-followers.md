# List User Followers with Are.na

Retrieves followers for a user in Are.na.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:id/followers`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [List User Followers](https://www.are.na/developers/explore/user/followers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Are.na user ID or slug. |
