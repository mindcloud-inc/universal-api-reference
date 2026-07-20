# List Aliases with Weights & Biases

Retrieves aliases from Weights & Biases.

## Endpoint

- **Method:** `GET`
- **Path:** `/aliases`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [List Aliases](https://docs.wandb.ai/weave/reference/service-api/objects/aliases-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | yes | W&B project identifier in entity/project format. |
