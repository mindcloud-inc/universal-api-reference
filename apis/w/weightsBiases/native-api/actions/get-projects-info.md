# Get Projects Info with Weights & Biases

Retrieves project identifiers from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/projects_info`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Get Projects Info](https://docs.wandb.ai/weave/reference/service-api/service/projects-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_ids[]` | body | `array<string>` | yes | External W&B project IDs in entity/project format. |
