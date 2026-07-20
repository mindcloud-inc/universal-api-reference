# Read Object with Weights & Biases

Retrieves an object version from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/obj/read`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Read Object](https://docs.wandb.ai/weave/reference/service-api/objects/obj-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `digest` | body | `string` | yes | The object version digest to read. |
| `object_id` | body | `string` | yes | The W&B Weave object ID to read. |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
