# Adjust Image Quality with change.photos

Creates an image with adjusted quality in change.photos.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/change`
- **Base URL:** `https://www.change.photos`
- **Official documentation:** [Adjust Image Quality](https://www.change.photos/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the image to process. |
| `quality` | body | `number` | yes | Output image quality from 1 to 100. |
