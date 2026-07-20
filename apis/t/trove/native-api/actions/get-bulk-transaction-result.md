# Get Bulk Transaction Result with Trove

Retrieves the result of a bulk enrichment request from Trove.

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions/bulk/:requestId`
- **Base URL:** `https://trove.headline.com/api/v1`
- **Official documentation:** [Get Bulk Transaction Result](https://trove.headline.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | The bulk request ID returned by Enrich Bulk Transactions. |
