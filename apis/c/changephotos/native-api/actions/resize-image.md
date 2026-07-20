# Resize Image with change.photos

Creates a resized image in change.photos.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/change`
- **Base URL:** `https://www.change.photos`
- **Official documentation:** [Resize Image](https://www.change.photos/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the image to resize. |
| `width` | body | `number` | yes | Desired width of the output image. |
| `height` | body | `number` | yes | Desired height of the output image. |
| `fit` | body | `list<string>` | no | How the image should fit within the dimensions. Accepted values: `contain`, `cover`, `fill`, `inside`, `outside`. |
