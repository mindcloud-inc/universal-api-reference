# Tint Image with change.photos

Creates a tinted image in change.photos.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/change`
- **Base URL:** `https://www.change.photos`
- **Official documentation:** [Tint Image](https://www.change.photos/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the image to tint. |
| `tint.r` | body | `number` | yes | Red component of the RGB tint, from 0 to 255. |
| `tint.g` | body | `number` | yes | Green component of the RGB tint, from 0 to 255. |
| `tint.b` | body | `number` | yes | Blue component of the RGB tint, from 0 to 255. |
