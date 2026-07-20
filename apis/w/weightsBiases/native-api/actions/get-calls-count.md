# Get Calls Count with Weights & Biases

Retrieves call counts from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/calls/query_stats`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Get Calls Count](https://docs.wandb.ai/weave/reference/service-api/calls/calls-query-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
