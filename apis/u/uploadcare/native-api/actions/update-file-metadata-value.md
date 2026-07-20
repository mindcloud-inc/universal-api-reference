# Update File Metadata Value with Uploadcare

Updates a file metadata value in Uploadcare.

## Endpoint

- **Method:** `PUT`
- **Path:** `/files/:uuid/metadata/:key/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Update File Metadata Value](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File-metadata/operation/updateFileMetadataKey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Metadata key name. |
| `uuid` | path | `string` | yes | Uploadcare file UUID. |
| `value` | body | `string` | yes | Metadata value to write for the selected key. |
