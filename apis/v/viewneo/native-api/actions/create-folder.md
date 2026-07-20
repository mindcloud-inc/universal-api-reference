# Create Folder with Viewneo

Creates a new media folder in Viewneo.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafile`
- **Base URL:** `https://cloud.viewneo.com/api/v1.0`
- **Official documentation:** [Create Folder](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.store.directory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media_file_id_as_parent_directory` | body | `number` | yes | ID of folder |
| `name` | body | `string` | yes | Name of directory |
