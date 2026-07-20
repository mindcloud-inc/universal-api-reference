# Create Gemini 2.5 Flash Image Task with PiAPI/NanoBanana

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Gemini 2.5 Flash Image Task](https://piapi.ai/docs/gemini-api/gemini-25-flash-image)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes |
| `input.output_format` | body | `string` | no |
| `input.aspect_ratio` | body | `string` | no |
| `config.webhook_config.endpoint` | body | `string` | no |
| `config.webhook_config.secret` | body | `string` | no |
