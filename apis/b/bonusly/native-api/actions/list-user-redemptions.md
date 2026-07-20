# List User Redemptions with Bonusly

Retrieves redemptions for a Bonusly user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/redemptions`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [List User Redemptions](https://docs.bonus.ly/reference/redemptions-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bonusly user ID whose redemptions to list. |
