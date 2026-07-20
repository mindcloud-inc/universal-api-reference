# Query Calls with Weights & Biases

Retrieves call records from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/calls/stream_query`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Query Calls](https://docs.wandb.ai/weave/reference/service-api/calls/calls-query-stream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
