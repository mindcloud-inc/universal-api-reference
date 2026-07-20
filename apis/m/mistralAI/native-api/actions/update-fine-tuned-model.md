# Update Fine Tuned Model with Mistral AI

Updates an existing fine-tuned model in Mistral AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/fine_tuning/models/:model_id`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Update Fine Tuned Model](https://docs.mistral.ai/api/endpoint/models#operation-jobs_api_routes_fine_tuning_update_fine_tuned_model)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | path | `string` | yes | The ID of the fine-tuned model. |
| `name` | body | `string` | no | Updated model name. |
| `description` | body | `string` | no | Updated model description. |
