# Get IDR Reprocess Status with Hightouch

Retrieves IDR reprocessing status from Hightouch.

## Endpoint

- **Method:** `GET`
- **Path:** `/idr/{graphId}/reprocess-status/{requestId}`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Get IDR Reprocess Status](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `graphId` | path | `string` | yes | The IDR graph ID. |
| `requestId` | path | `string` | yes | The IDR reprocessing request ID. |
