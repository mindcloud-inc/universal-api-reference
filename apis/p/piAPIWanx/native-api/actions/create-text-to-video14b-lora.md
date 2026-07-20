# Create Text to Video with LoRA with PiAPI/Wanx

Creates a LoRA text-to-video task in PiAPI/Wanx.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/task`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Create Text to Video with LoRA](https://piapi.ai/docs/wanx-api/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.prompt` | body | `string` | yes | Describe the video you want WanX to generate. |
| `input.negative_prompt` | body | `string` | no | Describe elements you want the model to avoid. |
| `input.aspect_ratio` | body | `string` | no | Supported ratios are 16:9 and 9:16. PiAPI defaults to 16:9. |
| `input.lora_settings[]` | body | `array<object>` | yes | Array of LoRA objects such as [{"lora_type":"ghibli","lora_strength":1.0}]. |
