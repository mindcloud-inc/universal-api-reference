# Query Feedback with Weights & Biases

Retrieves feedback records from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback/query`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Query Feedback](https://docs.wandb.ai/weave/reference/service-api/feedback/feedback-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
