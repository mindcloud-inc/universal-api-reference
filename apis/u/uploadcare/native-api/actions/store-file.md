# Store File with Uploadcare

Stores an existing file in Uploadcare.

## Endpoint

- **Method:** `PUT`
- **Path:** `/files/:uuid/storage/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Store File](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/storeFile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Uploadcare file UUID. |
