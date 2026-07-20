# Train Model with NextBrain

Starts training a model in NextBrain.

## Endpoint

- **Method:** `POST`
- **Path:** `/model/train_token`
- **Base URL:** `https://api.nextbrain.ai`
- **Official documentation:** [Train Model](https://api.nextbrain.ai/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | body | `string` | yes | The NextBrain model ID to train. |
| `target` | body | `string` | yes | The target column to train against. |
| `is_lightning` | body | `boolean` | no | Whether to request Lightning training mode. |
