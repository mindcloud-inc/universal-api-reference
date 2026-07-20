# Get Call Stats with Weights & Biases

Retrieves call statistics from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/calls/stats`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Get Call Stats](https://docs.wandb.ai/weave/reference/service-api/calls/call-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
