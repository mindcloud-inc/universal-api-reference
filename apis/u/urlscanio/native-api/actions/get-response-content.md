# Get Response Content with urlscan.io

## Endpoint

- **Method:** `GET`
- **Path:** `/responses/{fileHash}/`
- **Base URL:** `https://urlscan.io`
- **Official documentation:** [Get Response Content](https://docs.urlscan.io/apis/urlscan-openapi/scanning/response.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileHash` | path | `string` | no | The SHA256 hash of the response body to retrieve. |
