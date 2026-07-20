# Create Flux Text to Image Task with PiAPI/Flux.1

Creates a Flux text-to-image task in PiAPI/Flux.1.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Flux Text to Image Task](https://piapi.ai/docs/flux-api/text-to-image)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `input.prompt` | body | `string` | yes |
| `input.width` | body | `number` | no |
| `input.height` | body | `number` | no |
| `config.webhook_config.endpoint` | body | `string` | no |
| `config.webhook_config.secret` | body | `string` | no |
