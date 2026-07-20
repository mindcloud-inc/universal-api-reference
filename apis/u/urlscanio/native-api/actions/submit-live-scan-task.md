# Submit Live Scan Task with urlscan.io

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/livescan/{scannerId}/task/`
- **Base URL:** `https://urlscan.io`
- **Official documentation:** [Submit Live Scan Task](https://docs.urlscan.io/apis/urlscan-openapi/live-scanning/livescantask.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scannerId` | path | `string` | no | The live scanner node identifier. |
