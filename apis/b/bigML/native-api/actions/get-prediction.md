# Get Prediction with BigML

Retrieves a prediction from BigML.

## Endpoint

- **Method:** `GET`
- **Path:** `/prediction/:predictionId`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Get Prediction](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `predictionId` | path | `string` | yes | BigML prediction identifier suffix only (for example, 69cd1234abcd1234abcd1234). Do not include prediction/. |
