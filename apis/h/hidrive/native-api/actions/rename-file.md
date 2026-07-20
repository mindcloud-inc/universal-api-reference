# Rename File with HiDrive

Renames a file in HiDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/rename`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Rename File](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file/rename_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | no | File path to rename. |
| `pid` | body | `string` | no | File public ID. |
| `name` | body | `string` | yes | New file name. |
