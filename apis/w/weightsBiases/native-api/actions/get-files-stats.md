# Get Files Stats with Weights & Biases

Retrieves file storage statistics from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/query_stats`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Get Files Stats](https://docs.wandb.ai/weave/reference/service-api/files/files-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
