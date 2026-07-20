# Delete File with HiDrive

Deletes a file from HiDrive.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/file`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Delete File](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file_DELETE)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | no | File path to delete. |
| `pid` | body | `string` | no | File public ID. |
