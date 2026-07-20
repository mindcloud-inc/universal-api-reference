# Calculate Text-to-Video Price with deAPI

Calculates text-to-video request pricing in deAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/txt2video/price-calculation`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fps` | body | `string` | no | Frames per second for pricing. |
| `frames` | body | `string` | no | Number of frames to price. |
| `height` | body | `string` | no | Video height in pixels. |
| `model` | body | `string` | no | Video model slug from List Models. |
| `steps` | body | `string` | no | Number of inference steps. |
| `width` | body | `string` | no | Video width in pixels. |
