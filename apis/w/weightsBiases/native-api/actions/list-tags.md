# List Tags with Weights & Biases

Retrieves tags from Weights & Biases.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [List Tags](https://docs.wandb.ai/weave/reference/service-api/objects/tags-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | W&B project identifier in entity/project format. |
