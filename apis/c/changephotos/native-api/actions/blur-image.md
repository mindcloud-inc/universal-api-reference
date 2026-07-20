# Blur Image with change.photos

Creates a blurred image in change.photos.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/change`
- **Base URL:** `https://www.change.photos`
- **Official documentation:** [Blur Image](https://www.change.photos/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the image to blur. |
| `blur` | body | `number` | yes | Gaussian blur sigma value from 0.3 to 1000. |
