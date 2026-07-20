# Create Nano Banana Pro Task with PiAPI/NanoBanana

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Nano Banana Pro Task](https://piapi.ai/docs/gemini-api/nano-banana-pro)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes |
| `input.output_format` | body | `string` | no |
| `input.aspect_ratio` | body | `string` | no |
| `input.resolution` | body | `string` | no |
| `input.safety_level` | body | `string` | no |
| `config.webhook_config.endpoint` | body | `string` | no |
| `config.webhook_config.secret` | body | `string` | no |
