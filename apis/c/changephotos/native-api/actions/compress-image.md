# Compress Image with change.photos

Creates a compressed image in change.photos.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/change`
- **Base URL:** `https://www.change.photos`
- **Official documentation:** [Compress Image](https://www.change.photos/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the image to compress. |
| `format` | body | `list<string>` | no | Output image format. Accepted values: `jpeg`, `png`, `webp`. |
| `quality` | body | `number` | no | Output image quality from 1 to 100. |
