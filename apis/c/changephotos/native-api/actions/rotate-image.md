# Rotate Image with change.photos

Creates a rotated image in change.photos.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/change`
- **Base URL:** `https://www.change.photos`
- **Official documentation:** [Rotate Image](https://www.change.photos/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the image to rotate. |
| `rotate` | body | `number` | yes | Rotation angle in degrees from -360 to 360. |
