# Create Prediction with Muna

Creates a prediction in Muna for a predictor tag.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/predictions`
- **Base URL:** `https://api.muna.ai`
- **Official documentation:** [Create Prediction](https://docs.muna.ai/ref/predictions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | body | `string` | yes | Predictor tag. |
| `clientId` | body | `string` | yes | Prediction client identifier. |
| `configurationId` | body | `string` | no | Prediction configuration identifier. |
| `deviceId` | body | `string` | no | Device identifier, used for choosing optimal implementation to respond with. |
| `predictionId` | body | `string` | no | Original prediction identifier for embedded predictors. |
