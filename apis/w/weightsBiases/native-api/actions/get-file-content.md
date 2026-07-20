# Get File Content with Weights & Biases

Retrieves file content from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/content`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Get File Content](https://docs.wandb.ai/weave/reference/service-api/files/file-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `digest` | body | `string` | yes | The file digest to fetch content for. |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
