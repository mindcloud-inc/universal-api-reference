# Replicate Create Prediction with CometAPI

Creates a Replicate prediction in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/replicate/v1/models/:models/predictions`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Replicate Create Prediction](https://apidoc.cometapi.com/api/image/replicate/create-predictions-general)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `object` | yes | Prediction input object. |
| `models` | path | `string` | yes | Replicate model path. |
