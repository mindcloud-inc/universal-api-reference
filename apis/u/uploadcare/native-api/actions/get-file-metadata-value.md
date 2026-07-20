# Get File Metadata Value with Uploadcare

Retrieves a file metadata value from Uploadcare by key.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:uuid/metadata/:key/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Get File Metadata Value](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File-metadata/operation/fileMetadataKey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Metadata key name. |
| `uuid` | path | `string` | yes | Uploadcare file UUID. |
