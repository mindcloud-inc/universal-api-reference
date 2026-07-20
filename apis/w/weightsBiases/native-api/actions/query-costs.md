# Query Costs with Weights & Biases

Retrieves cost records from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/cost/query`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Query Costs](https://docs.wandb.ai/weave/reference/service-api/costs/cost-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
