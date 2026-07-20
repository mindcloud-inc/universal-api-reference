# Generate Audio with PiAPI/MMAudio

Creates an MMAudio audio generation task in PiAPI/MMAudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Generate Audio](https://piapi.ai/docs/mmaudio-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.video` | body | `string` | yes | Public video URL to send to PiAPI MMAudio. |
| `input.prompt` | body | `string` | no | — |
| `input.negative_prompt` | body | `string` | no | — |
| `input.steps` | body | `number` | no | — |
| `input.seed` | body | `number` | no | — |
| `config.webhook_config.endpoint` | body | `string` | no | — |
| `config.webhook_config.secret` | body | `string` | no | — |
