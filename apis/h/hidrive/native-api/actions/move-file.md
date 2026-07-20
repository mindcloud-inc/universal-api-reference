# Move File with HiDrive

Moves a file in HiDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/move`
- **Base URL:** `https://api.hidrive.strato.com/2.1`
- **Official documentation:** [Move File](https://api.hidrive.strato.com/2.1/static/apidoc/index.html#/2.1/file/move_POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dst_id` | body | `string` | no | Destination parent public ID. |
| `src` | body | `string` | no | Source file path. |
| `src_id` | body | `string` | no | Source file public ID. |
| `dst` | body | `string` | yes | Destination file path. |
