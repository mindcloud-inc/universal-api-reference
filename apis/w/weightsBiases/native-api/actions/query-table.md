# Query Table with Weights & Biases

Retrieves table rows from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/table/query`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Query Table](https://docs.wandb.ai/weave/reference/service-api/tables/table-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `digest` | body | `string` | yes | The table digest to query. |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
