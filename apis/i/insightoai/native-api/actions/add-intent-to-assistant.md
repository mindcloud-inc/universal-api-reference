# Add Intent To Assistant with Insighto.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/assistant/:assistant_id/intent/:intent_id`
- **Base URL:** `https://api.insighto.ai/api/v1`
- **Official documentation:** [Add Intent To Assistant](https://docs.insighto.ai/api-reference/assistant/add-intent-to-assistant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assistant_id` | path | `string` | yes | The UUID id of the assistant. |
| `intent_id` | path | `string` | yes | The UUID id of the intent. |
