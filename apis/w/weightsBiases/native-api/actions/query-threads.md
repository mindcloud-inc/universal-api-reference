# Query Threads with Weights & Biases

Retrieves threads from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/threads/stream_query`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Query Threads](https://docs.wandb.ai/weave/reference/service-api/threads/threads-query-stream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
