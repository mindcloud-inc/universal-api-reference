# Get Predict Columns with NextBrain

Retrieves prediction columns for a NextBrain model.

## Endpoint

- **Method:** `POST`
- **Path:** `/model/predict_columns_token/:model_id`
- **Base URL:** `https://api.nextbrain.ai`
- **Official documentation:** [Get Predict Columns](https://api.nextbrain.ai/docs)

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
