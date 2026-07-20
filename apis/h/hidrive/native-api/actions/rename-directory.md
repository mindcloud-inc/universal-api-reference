# Rename Directory with HiDrive

Renames a directory in HiDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/dir/rename`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Rename Directory](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir/rename_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | body | `string` | no | Directory path to rename. |
| `pid` | body | `string` | no | Directory public ID. |
| `name` | body | `string` | yes | New directory name. |
