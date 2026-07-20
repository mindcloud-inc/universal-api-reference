# Run Live Scan with urlscan.io

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/livescan/{scannerId}/scan/`
- **Base URL:** `https://urlscan.io`
- **Official documentation:** [Run Live Scan](https://docs.urlscan.io/apis/urlscan-openapi/live-scanning/livescanscan.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scannerId` | path | `string` | no | The live scanner node identifier. |
