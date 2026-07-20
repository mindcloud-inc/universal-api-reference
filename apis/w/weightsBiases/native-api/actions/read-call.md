# Read Call with Weights & Biases

Retrieves a call record from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/call/read`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Read Call](https://docs.wandb.ai/weave/reference/service-api/calls/call-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The W&B Weave call ID to read. |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
