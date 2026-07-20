# Get Bulk Run with Browse AI

Retrieves a bulk run from Browse AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/robots/:robotId/bulk-runs/:bulkRunId`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [Get Bulk Run](https://developers.browse.ai/v2#tag/bulk-runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `bulkRunId` | path | `string` | yes | Unique bulk run ID |
| `page` | query | `number` | no | Page number |
