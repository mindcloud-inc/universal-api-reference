# List User Groups with Are.na

Retrieves groups for a user in Are.na.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:id/groups`
- **Base URL:** `https://api.are.na/v3`
- **Official documentation:** [List User Groups](https://www.are.na/developers/explore/user/groups)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Are.na user ID or slug. |
