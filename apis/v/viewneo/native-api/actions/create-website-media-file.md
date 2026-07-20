# Create Website Media File with Viewneo

Creates a new website media file in Viewneo.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafile`
- **Base URL:** `https://cloud.viewneo.com/api/v1.0`
- **Official documentation:** [Create Website Media File](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.store.website)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media_file_id_as_parent_directory` | body | `number` | yes | ID of folder |
| `url` | body | `string` | yes | URL of website |
