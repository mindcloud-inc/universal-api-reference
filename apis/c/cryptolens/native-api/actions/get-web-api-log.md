# Get Web API Log with Cryptolens

Retrieves Web API logs from Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ai/GetWebAPILog`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Get Web API Log](https://app.cryptolens.io/docs/api/v3/GetWebAPILog)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | no | Product ID to filter on. |
| `Key` | query | `string` | no | License key string to filter on. |
| `MachineCode` | query | `string` | no | Machine code to filter on. |
| `FriendlyName` | query | `string` | no | Friendly name filter. |
| `States` | query | `string` | no | JSON list of integer state codes to filter on. |
| `Time` | query | `string` | no | JSON interval filter for request time. |
| `Limit` | query | `number` | no | Maximum number of logs to return. |
| `StartingAfter` | query | `string` | no | Cursor for logs after the given id. |
| `EndingBefore` | query | `string` | no | Cursor for logs before the given id. |
| `OrderBy` | query | `string` | no | Ordering value such as Id descending. |
| `AnomalyClassification` | query | `boolean` | no | Whether to include anomaly classification details. |
| `v` | query | `string` | no | Method version. |
