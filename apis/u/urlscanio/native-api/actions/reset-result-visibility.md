# Reset Result Visibility with urlscan.io

Deletes a scan result visibility override in urlscan.io.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/result/{scanId}/visibility/`
- **Base URL:** `https://urlscan.io`
- **Official documentation:** [Reset Result Visibility](https://docs.urlscan.io/apis/urlscan-openapi/scanning/deleteresultvisibility.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scanId` | path | `string` | no | The scan UUID whose visibility you want to reset. |
