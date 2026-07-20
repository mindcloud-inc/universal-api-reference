# Get Model Status with NextBrain

Retrieves a model status from NextBrain.

## Endpoint

- **Method:** `POST`
- **Path:** `/model/status_token/:model_id`
- **Base URL:** `https://api.nextbrain.ai`
- **Official documentation:** [Get Model Status](https://api.nextbrain.ai/docs)

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
