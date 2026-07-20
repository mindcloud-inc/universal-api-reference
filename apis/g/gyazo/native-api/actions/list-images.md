# List Images with Gyazo

Retrieves images from Gyazo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/images`
- **Base URL:** `https://api.gyazo.com`
- **Official documentation:** [List Images](https://gyazo.com/api/docs/image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. |
| `per_page` | query | `number` | no | Number of images to return, from 1 to 100. |
