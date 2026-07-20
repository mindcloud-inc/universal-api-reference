# Delete File with Uploadcare

Deletes an existing file from Uploadcare storage.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/files/:uuid/storage/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Delete File](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/deleteFileStorage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Uploadcare file UUID. |
