# Get Table Stats with Weights & Biases

Retrieves table statistics from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/table/query_stats`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Get Table Stats](https://docs.wandb.ai/weave/reference/service-api/tables/table-query-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `digest` | body | `string` | yes | The table digest to summarize. |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
