# Get Calls Usage with Weights & Biases

Retrieves call usage metrics from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/calls/usage`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Get Calls Usage](https://docs.wandb.ai/weave/reference/service-api/calls/calls-usage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
