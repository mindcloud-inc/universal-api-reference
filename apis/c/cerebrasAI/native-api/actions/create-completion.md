# Create Completion with Cerebras AI

Creates a completion in Cerebras AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/completions`
- **Base URL:** `https://api.cerebras.ai`
- **Official documentation:** [Create Completion](https://inference-docs.cerebras.ai/api-reference/completions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `prompt` | body | `string` | no |
| `max_tokens` | body | `number` | no |
