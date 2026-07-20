# Create DeepResearch Task with Valyu

## Endpoint

- **Method:** `POST`
- **Path:** `/deepresearch/tasks`
- **Base URL:** `https://api.valyu.ai/v1`
- **Official documentation:** [Create DeepResearch Task](https://docs.valyu.ai/api-reference/endpoint/deepresearch-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | body | `string` | no | Research mode controlling depth and cost. |
| `query` | body | `string` | yes | The research query or question. |
