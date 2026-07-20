# Delete Model with NextBrain

Deletes an existing model from NextBrain.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/model/delete_model_token/:model_id`
- **Base URL:** `https://api.nextbrain.ai`
- **Official documentation:** [Delete Model](https://api.nextbrain.ai/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | path | `string` | yes | The NextBrain model ID to delete. |
