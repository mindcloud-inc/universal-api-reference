# Update DeepResearch Task with Valyu

## Endpoint

- **Method:** `POST`
- **Path:** `/deepresearch/tasks/:id/update`
- **Base URL:** `https://api.valyu.ai/v1`
- **Official documentation:** [Update DeepResearch Task](https://docs.valyu.ai/api-reference/endpoint/deepresearch-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The DeepResearch task ID. |
| `instruction` | body | `string` | yes | Follow-up instruction for the research agent. |
