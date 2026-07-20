# Create Flux Text to Image LoRA Task with PiAPI/Flux.1

Creates a Flux text-to-image LoRA task in PiAPI/Flux.1.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Flux Text to Image LoRA Task](https://piapi.ai/docs/flux-with-lora-and-controlnet)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes |
| `input.lora_settings[]` | body | `array` | yes |
| `config.webhook_config.endpoint` | body | `string` | no |
| `config.webhook_config.secret` | body | `string` | no |
