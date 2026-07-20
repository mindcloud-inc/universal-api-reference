# Create Response with SEA-LION AI Playground

## Endpoint

- **Method:** `POST`
- **Path:** `/responses`
- **Base URL:** `https://api.sea-lion.ai/v1`
- **Official documentation:** [Create Response](https://api.sea-lion.ai/openapi.json)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `input` | body | `string` | yes |
| `instructions` | body | `string` | no |
| `temperature` | body | `number` | no |
| `max_output_tokens` | body | `number` | no |
| `stream` | body | `boolean` | no |
