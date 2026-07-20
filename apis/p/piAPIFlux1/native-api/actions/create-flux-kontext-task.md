# Create Flux Kontext Task with PiAPI/Flux.1

Creates a Flux Kontext task in PiAPI/Flux.1.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Flux Kontext Task](https://piapi.ai/docs/flux-api/kontext)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes |
| `input.image` | body | `string` | yes |
| `input.width` | body | `number` | no |
| `input.height` | body | `number` | no |
| `input.steps` | body | `number` | no |
| `input.seed` | body | `number` | no |
| `config.webhook_config.endpoint` | body | `string` | no |
| `config.webhook_config.secret` | body | `string` | no |
