# Create Image Edit Task with PiAPI/Qwen

Creates an image edit task in PiAPI/Qwen.

## Endpoint

- **Method:** `POST`
- **Path:** `/task`
- **Base URL:** `https://api.piapi.ai/api/v1`
- **Official documentation:** [Create Image Edit Task](https://piapi.ai/docs/qwen-image-api/image-edit)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input.image1` | body | `string` | yes |
| `input.image2` | body | `string` | no |
| `input.image3` | body | `string` | no |
| `input.prompt` | body | `string` | yes |
| `input.negative_prompt` | body | `string` | no |
| `input.seed` | body | `number` | no |
| `input.steps` | body | `number` | no |
| `input.flow_shift` | body | `number` | no |
| `config.webhook_config.endpoint` | body | `string` | no |
| `config.webhook_config.secret` | body | `string` | no |
