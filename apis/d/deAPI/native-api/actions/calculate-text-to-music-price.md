# Calculate Text-to-Music Price with deAPI

Calculates text-to-music request pricing in deAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/txt2music/price-calculation`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | body | `string` | no | Music duration in seconds. |
| `inference_steps` | body | `string` | no | Number of diffusion inference steps. |
| `model` | body | `string` | no | Music model slug from List Models. |
