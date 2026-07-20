# Move Directory with HiDrive

Moves a directory in HiDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/dir/move`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Move Directory](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/dir/move_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dst_id` | body | `string` | no | Destination parent public ID. |
| `src` | body | `string` | no | Source directory path. |
| `src_id` | body | `string` | no | Source directory public ID. |
| `dst` | body | `string` | yes | Destination directory path. |
