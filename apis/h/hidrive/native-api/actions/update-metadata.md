# Update Metadata with HiDrive

Updates file metadata in HiDrive.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/meta`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Update Metadata](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/meta_PATCH)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | no | File or folder path. |
| `pid` | body | `string` | no | HiDrive public ID for the object. |
| `mtime` | body | `number` | yes | Unix timestamp to set as object modification time. |
