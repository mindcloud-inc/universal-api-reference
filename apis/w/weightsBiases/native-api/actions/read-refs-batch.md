# Read Refs Batch with Weights & Biases

Retrieves refs in batch from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/refs/read_batch`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Read Refs Batch](https://docs.wandb.ai/weave/reference/service-api/refs/refs-read-batch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
| `refs` | body | `list<string>` | yes | W&B refs to resolve in a batch. Send multiple values as a array. |
