# Create Flux ControlNet LoRA Task with PiAPI/Flux.1

Creates a Flux ControlNet LoRA task in PiAPI/Flux.1.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Flux ControlNet LoRA Task](https://piapi.ai/docs/flux-with-lora-and-controlnet)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes |
| `input.control_net_settings[]` | body | `array` | yes |
| `input.lora_settings[]` | body | `array` | no |
| `input.steps` | body | `number` | no |
| `input.negative_prompt` | body | `string` | no |
| `input.guidance_scale` | body | `number` | no |
| `config.webhook_config.endpoint` | body | `string` | no |
| `config.webhook_config.secret` | body | `string` | no |
