# Create Directory with HiDrive

Creates a new directory in HiDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/dir`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Create Directory](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `on_exist` | body | `string` | no | Conflict behavior, such as autoname. |
| `path` | body | `string` | yes | Directory path to create. |
| `pid` | body | `string` | no | Optional parent directory public ID. |
