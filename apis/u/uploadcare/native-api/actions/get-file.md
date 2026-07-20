# Get File with Uploadcare

Retrieves a file record from Uploadcare.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:uuid/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Get File](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/fileInfo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Include additional file fields such as appdata. |
| `uuid` | path | `string` | yes | Uploadcare file UUID. |
