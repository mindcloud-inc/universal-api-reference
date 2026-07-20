# Add Inputs To Dataset with Clarifai

Adds inputs to a dataset in Clarifai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/users/me/apps/:appId/datasets/:datasetId/inputs`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Add Inputs To Dataset](https://docs.clarifai.com/create/datasets/upload/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `datasetId` | path | `string` | yes | Clarifai dataset ID. |
| `dataset_inputs[]` | body | `array<object>` | yes | Inputs to add to the dataset. |
| `dataset_inputs[].input` | body | `object` | no | Input reference. |
| `dataset_inputs[].input.id` | body | `string` | yes | Existing Clarifai input ID. |
