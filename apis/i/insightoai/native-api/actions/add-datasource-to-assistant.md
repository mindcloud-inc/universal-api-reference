# Add Datasource To Assistant with Insighto.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/assistant/:assistant_id/data_source/:datasource_id`
- **Base URL:** `https://api.insighto.ai/api/v1`
- **Official documentation:** [Add Datasource To Assistant](https://docs.insighto.ai/api-reference/assistant/add-datasource-to-assistant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assistant_id` | path | `string` | yes | The UUID id of the assistant. |
| `datasource_id` | path | `string` | yes | The UUID id of the datasource. |
