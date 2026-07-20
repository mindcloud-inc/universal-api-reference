# Get DOM Snapshot with urlscan.io

Retrieves a scan DOM snapshot from urlscan.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/dom/{scanId}/`
- **Base URL:** `https://urlscan.io`
- **Official documentation:** [Get DOM Snapshot](https://docs.urlscan.io/apis/urlscan-openapi/scanning/dom.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scanId` | path | `string` | no | The scan UUID returned by urlscan. |
