# Delete Directory with HiDrive

Deletes a directory from HiDrive.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/dir`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Delete Directory](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir_DELETE)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | no | Directory path to delete. |
| `pid` | body | `string` | no | Directory public ID. |
| `recursive` | body | `boolean` | no | Delete non-empty directory contents recursively. |
