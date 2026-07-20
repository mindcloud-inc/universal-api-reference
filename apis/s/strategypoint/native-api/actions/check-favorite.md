# Check Favorite with Strategypoint

Checks favorites in Strategypoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/favorites`
- **Base URL:** `https://app.clearpointstrategy.com/api/v1`
- **Official documentation:** [Check Favorite](https://developer.clearpointstrategy.com/reference/checkfavorite-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `layoutId` | query | `number` | no | The layout identifier to check. |
| `object` | query | `string` | yes | The object type to check for a favorite entry. |
| `objectId` | query | `number` | no | The object identifier to check. |
