# Update Result Visibility with urlscan.io

Updates a scan result's visibility in urlscan.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/result/{scanId}/visibility/`
- **Base URL:** `https://urlscan.io`
- **Official documentation:** [Update Result Visibility](https://docs.urlscan.io/apis/urlscan-openapi/scanning/updateresultvisibility.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scanId` | path | `string` | no | The scan UUID whose visibility you want to update. |
