# Create Response with Groq

Creates a response in Groq.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/v1/responses`
- **Base URL:** `https://api.groq.com`
- **Official documentation:** [Create Response](https://console.groq.com/docs/api-reference#responses-create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `input` | body | `string` | yes |
| `instructions` | body | `string` | no |
| `max_output_tokens` | body | `number` | no |
| `temperature` | body | `number` | no |
| `stream` | body | `boolean` | no |
| `user` | body | `string` | no |
| `reasoning.effort` | body | `list` | no |
| `metadata` | body | `object` | no |
| `parallel_tool_calls` | body | `boolean` | no |
| `service_tier` | body | `list` | no |
| `store` | body | `boolean` | no |
| `top_p` | body | `number` | no |
| `truncation` | body | `list` | no |
