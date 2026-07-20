# Copy File with HiDrive

Copies a file in HiDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/copy`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Copy File](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file/copy_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dst_id` | body | `string` | no | Destination parent public ID. |
| `on_exist` | body | `string` | no | Conflict behavior, such as autoname. |
| `src` | body | `string` | no | Source file path. |
| `src_id` | body | `string` | no | Source file public ID. |
| `dst` | body | `string` | yes | Destination file path. |
