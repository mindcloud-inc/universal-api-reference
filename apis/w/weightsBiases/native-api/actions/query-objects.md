# Query Objects with Weights & Biases

Retrieves object versions from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/objs/query`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Query Objects](https://docs.wandb.ai/weave/reference/service-api/objects/objs-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
