# Create Text to Image Task with PiAPI/Qwen

Creates a text-to-image task in PiAPI/Qwen.

## Endpoint

- **Method:** `POST`
- **Path:** `/task`
- **Base URL:** `https://api.piapi.ai/api/v1`
- **Official documentation:** [Create Text to Image Task](https://piapi.ai/docs/qwen-image-api/text-to-image)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes |
| `input.seed` | body | `number` | no |
| `input.steps` | body | `number` | no |
| `input.width` | body | `number` | no |
| `input.height` | body | `number` | no |
| `input.flow_shift` | body | `number` | no |
| `config.webhook_config.endpoint` | body | `string` | no |
| `config.webhook_config.secret` | body | `string` | no |
