# List Goal Conversions with condoo

Retrieves goal conversions from condoo.

## Endpoint

- **Method:** `GET`
- **Path:** `/goals-conversions/`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [List Goal Conversions](https://trk.condoo.systems/en/api-documentation/goals-conversions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `goal_id` | query | `number` | no | Optional goal ID selector. |
| `website_id` | query | `number` | no | Optional website ID selector. |
