# Get Feedback Stats with Weights & Biases

Retrieves feedback statistics from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback/stats`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Get Feedback Stats](https://docs.wandb.ai/weave/reference/service-api/feedback/feedback-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
