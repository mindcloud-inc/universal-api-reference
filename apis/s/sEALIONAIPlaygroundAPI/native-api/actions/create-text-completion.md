# Create Text Completion with SEA-LION AI Playground

## Endpoint

- **Method:** `POST`
- **Path:** `/completions`
- **Base URL:** `https://api.sea-lion.ai/v1`
- **Official documentation:** [Create Text Completion](https://api.sea-lion.ai/openapi.json)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `prompt` | body | `string` | yes |
| `temperature` | body | `number` | no |
| `max_tokens` | body | `number` | no |
