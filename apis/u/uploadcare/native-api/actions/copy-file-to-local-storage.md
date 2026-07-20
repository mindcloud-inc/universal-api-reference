# Copy File To Local Storage with Uploadcare

Creates a local storage copy in Uploadcare.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/local_copy/`
- **Base URL:** `https://api.uploadcare.com`
- **Official documentation:** [Copy File To Local Storage](https://uploadcare.com/api-refs/rest-api/v0.7.0/#tag/File/operation/createLocalCopy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadata` | body | `object` | no | Metadata object to attach to the copied file. |
| `source` | body | `string` | yes | Source file UUID or URL to copy into local storage. |
| `store` | body | `string` | no | Whether to store the copied file permanently. |
