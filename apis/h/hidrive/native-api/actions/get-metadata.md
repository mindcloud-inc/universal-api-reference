# Get Metadata with HiDrive

Retrieves file metadata from HiDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/meta`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Get Metadata](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/meta_GET)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated metadata fields to include. |
| `path` | query | `string` | no | File or folder path. |
| `pid` | query | `string` | no | HiDrive public ID for the object. |
