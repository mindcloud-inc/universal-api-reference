# Get Feedback Payload Schema with Weights & Biases

Retrieves feedback payload schema from Weights & Biases.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback/payload_schema`
- **Base URL:** `https://trace.wandb.ai`
- **Official documentation:** [Get Feedback Payload Schema](https://docs.wandb.ai/weave/reference/service-api/feedback/feedback-payload-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | W&B project identifier in entity/project format. |
