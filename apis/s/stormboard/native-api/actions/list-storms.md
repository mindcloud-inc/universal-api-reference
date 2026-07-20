# List Storms with Stormboard

Retrieves your Storms from Stormboard.

## Endpoint

- **Method:** `GET`
- **Path:** `/storms/list`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [List Storms](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | query | `number` | no | Filter storms by dashboard folder ID. |
| `needle` | query | `string` | no | Filter storms by storm title text. |
| `order` | query | `string` | no | Order by activity, alpha, frequency, or starred. |
| `results` | query | `number` | no | Maximum number of storms to return. |
| `start` | query | `number` | no | Start the result list at this index. |
| `status` | query | `string` | no | Filter by storm status: open or closed. |
| `team` | query | `number` | no | Filter storms by team ID. |
