# Create Text to Video with LoRA Task with PiAPI/Hunyuan

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Text to Video with LoRA Task](https://piapi.ai/docs/hunyuan-api-doc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes |
| `input.lora_settings[]` | body | `array<object>` | yes |
