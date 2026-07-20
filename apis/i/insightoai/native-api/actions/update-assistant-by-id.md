# Update Assistant By Id with Insighto.ai

## Endpoint

- **Method:** `PUT`
- **Path:** `/assistant/:assistant_id`
- **Base URL:** `https://api.insighto.ai/api/v1`
- **Official documentation:** [Update Assistant By Id](https://docs.insighto.ai/api-reference/assistant/update-assistant-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assistant_id` | path | `string` | yes | The UUID id of the assistant. |
| `assistant_type` | body | `list<string>` | no | Assistant type to update. Accepted values: `chat`, `nl2sql`, `phone`, `realtime_openai`, `simple`. |
| `llm_model` | body | `list<string>` | no | Foundation model used by the assistant. Accepted values: `deepseek-r1-distill-llama-70b`, `gpt-3.5-turbo`, `gpt-3.5-turbo-0125`, `gpt-3.5-turbo-1106`, `gpt-4-0125-preview`, `gpt-4-1106-preview`, `gpt-4o-2024-05-13`, `gpt-4o-mini`, `gpt-4o-mini-realtime-preview`, `gpt-4o-realtime-preview`, `llama-3.1-70b-versatile`, `o3-mini`. |
| `name` | body | `string` | no | Assistant name. |
