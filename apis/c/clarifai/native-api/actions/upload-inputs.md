# Upload Inputs with Clarifai

Uploads inputs to an app in Clarifai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/users/me/apps/:appId/inputs`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Upload Inputs](https://docs.clarifai.com/create/inputs/upload/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `inputs[]` | body | `array<object>` | no | Inputs to upload. |
| `inputs[].id` | body | `string` | no | Input ID. |
| `inputs[].data` | body | `object` | no | Input data. |
| `inputs[].data.image` | body | `object` | no | Image payload. |
| `inputs[].data.image.url` | body | `string` | no | Image URL to upload. |
| `inputs[].data.concepts[]` | body | `array<object>` | no | Concept annotations. |
| `inputs[].data.image.base64` | body | `string` | no | Base64-encoded image bytes. |
| `inputs[].data.concepts[].id` | body | `string` | no | Concept ID. |
| `inputs[].data.concepts[].value` | body | `number` | no | Concept score or label value. |
