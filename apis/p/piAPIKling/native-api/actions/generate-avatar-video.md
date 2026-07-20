# Generate Avatar Video with PiAPI/Kling

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Avatar Video](https://piapi.ai/docs/kling-api/kling-avatar-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.image_url` | body | `string` | yes | Source avatar image URL. |
| `input.local_dubbing_url` | body | `string` | yes | Audio URL to drive the avatar speech. |
| `input.prompt` | body | `string` | no | Optional prompt to guide the avatar delivery. |
| `input.mode` | body | `string` | no | Avatar generation mode, such as std or pro. |
| `input.batch_size` | body | `number` | no | Number of avatar outputs to request. |
