# Get File Metadata with Uploadcare

Retrieves all file metadata from Uploadcare.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:uuid/metadata/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Get File Metadata](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File-metadata/operation/_fileMetadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Uploadcare file UUID. |
