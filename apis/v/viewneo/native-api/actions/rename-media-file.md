# Rename Media File with Viewneo

Updates a media file name in Viewneo.

## Endpoint

- **Method:** `POST`
- **Path:** `/mediafile/:id`
- **Base URL:** `https://cloud.viewneo.com/api/v1.0`
- **Official documentation:** [Rename Media File](https://cloud.viewneo.com/doc/api#/MediaFile/api.mediaFile.update.rename)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `name` | body | `string` | yes |
