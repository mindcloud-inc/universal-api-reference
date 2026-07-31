# List Popular Memes with Imgflip

## Endpoint

- **Method:** `GET`
- **Path:** `/get_memes`
- **Base URL:** `https://api.imgflip.com`
- **Official documentation:** [List Popular Memes](https://imgflip.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `list` | no | Optional type: image, gif, or the documented comma-separated combination such as gif,image. Defaults to image. Accepted values: `gif`, `gif,image`, `image`. |
