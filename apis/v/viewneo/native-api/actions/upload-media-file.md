# Upload Media File with Viewneo

Uploads a media file to Viewneo.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafile`
- **Base URL:** `https://cloud.viewneo.com/api/v1.0`
- **Official documentation:** [Upload Media File](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.store.physical)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media_file_id_as_parent_directory` | body | `number` | yes | ID of folder |
| `file` | body | `file` | yes | File to upload |
