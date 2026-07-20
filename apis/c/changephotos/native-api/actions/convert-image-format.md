# Convert Image Format with change.photos

Creates an image in a new format in change.photos.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/change`
- **Base URL:** `https://www.change.photos`
- **Official documentation:** [Convert Image Format](https://www.change.photos/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the image to convert. |
| `format` | body | `list<string>` | yes | Output image format. Accepted values: `jpeg`, `png`, `webp`. |
