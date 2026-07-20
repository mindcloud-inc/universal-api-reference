# Copy Directory with HiDrive

Copies a directory in HiDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/dir/copy`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Copy Directory](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir/copy_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dst_id` | body | `string` | no | Destination parent public ID. |
| `on_exist` | body | `string` | no | Conflict behavior, such as autoname. |
| `src` | body | `string` | no | Source directory path. |
| `src_id` | body | `string` | no | Source directory public ID. |
| `dst` | body | `string` | yes | Destination directory path. |
