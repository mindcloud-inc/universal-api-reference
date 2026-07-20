# Delete File Metadata Key with Uploadcare

Deletes a file metadata key from Uploadcare.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/files/:uuid/metadata/:key/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Delete File Metadata Key](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File-metadata/operation/deleteFileMetadataKey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Metadata key name. |
| `uuid` | path | `string` | yes | Uploadcare file UUID. |
