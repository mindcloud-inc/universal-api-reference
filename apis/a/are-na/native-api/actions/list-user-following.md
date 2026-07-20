# List User Following with Are.na

Retrieves who a user follows in Are.na.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:id/following`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [List User Following](https://www.are.na/developers/explore/user/following)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Are.na user ID or slug. |
| `type` | query | `string` | no | Optional following type filter. |
