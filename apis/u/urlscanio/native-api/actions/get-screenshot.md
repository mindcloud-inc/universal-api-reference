# Get Screenshot with urlscan.io

Retrieves a scan screenshot from urlscan.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshots/{scanId}.png`
- **Base URL:** `https://urlscan.io`
- **Official documentation:** [Get Screenshot](https://docs.urlscan.io/apis/urlscan-openapi/scanning/screenshot.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scanId` | path | `string` | no | The scan UUID returned by urlscan. |
