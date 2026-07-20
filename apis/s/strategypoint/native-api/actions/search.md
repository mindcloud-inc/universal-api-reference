# Search with Strategypoint

Finds matching elements in Strategypoint.

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://app.clearpointstrategy.com/api/v1`
- **Official documentation:** [Search](https://developer.clearpointstrategy.com/reference/search-5)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Maximum number of results to return. |
| `object` | query | `string` | no | Limit search to a related object type. |
| `page` | query | `number` | no | Page number to return. |
| `periodId` | query | `number` | no | Limit search to a period. |
| `scorecardId` | query | `number` | no | Limit search to a scorecard. |
| `type` | query | `string` | no | Limit search to a specific result type. |
