# Get Model Accuracy with NextBrain

Retrieves model accuracy metrics from NextBrain.

## Endpoint

- **Method:** `POST`
- **Path:** `/model/acc_token/:model_id`
- **Base URL:** `https://api.nextbrain.ai`
- **Official documentation:** [Get Model Accuracy](https://api.nextbrain.ai/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | path | `string` | yes | The NextBrain model ID. |
