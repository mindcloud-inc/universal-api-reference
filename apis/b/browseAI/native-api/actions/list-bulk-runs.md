# List Bulk Runs with Browse AI

Retrieves bulk runs from Browse AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/robots/:robotId/bulk-runs`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [List Bulk Runs](https://developers.browse.ai/v2#tag/bulk-runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `page` | query | `number` | no | Page number |
