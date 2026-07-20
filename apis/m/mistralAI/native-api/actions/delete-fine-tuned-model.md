# Delete Fine Tuned Model with Mistral AI

Deletes an existing fine-tuned model from Mistral AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/models/:model_id`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Delete Fine Tuned Model](https://docs.mistral.ai/api/endpoint/models#operation-delete_model_v1_models_model_id_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | path | `string` | yes | The ID of the model to delete. |
