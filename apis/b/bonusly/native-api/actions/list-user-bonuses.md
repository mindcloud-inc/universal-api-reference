# List User Bonuses with Bonusly

Retrieves bonuses for a Bonusly user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/bonuses`
- **Base URL:** `https://bonus.ly/api/v1`
- **Official documentation:** [List User Bonuses](https://docs.bonus.ly/reference/bonuses-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bonusly user ID whose bonuses to list. |
