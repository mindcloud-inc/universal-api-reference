# Calculate Image Prompt Price with deAPI

Calculates image prompt enhancement pricing in deAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/prompt/image/price-calculation`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `negative_prompt` | body | `string` | no | Optional negative prompt to include in the estimate. |
| `prompt` | body | `string` | no | Image prompt to estimate enhancement cost for. |
