# Get Batch Prediction with BigML

Retrieves a batch prediction from BigML.

## Endpoint

- **Method:** `GET`
- **Path:** `/batchprediction/:batchPredictionId`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Get Batch Prediction](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchPredictionId` | path | `string` | yes | BigML batch prediction identifier suffix only (for example, 69cd1234abcd1234abcd1234). Do not include batchprediction/. |
