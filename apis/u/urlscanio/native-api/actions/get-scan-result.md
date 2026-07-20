# Get Scan Result with urlscan.io

Retrieves a scan result from urlscan.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/result/{scanId}/`
- **Base URL:** `https://urlscan.io`
- **Official documentation:** [Get Scan Result](https://docs.urlscan.io/apis/urlscan-openapi/scanning/resultapi.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scanId` | path | `string` | no | The scan UUID returned by urlscan. |
