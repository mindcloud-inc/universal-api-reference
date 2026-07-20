# Create Dataset Version with Clarifai

Creates a dataset version in Clarifai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/users/me/apps/:appId/datasets/:datasetId/versions`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Create Dataset Version](https://docs.clarifai.com/create/datasets/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `datasetId` | path | `string` | yes | Clarifai dataset ID. |
| `dataset_versions[]` | body | `array<object>` | yes | Dataset versions to create. |
| `dataset_versions[].id` | body | `string` | yes | Dataset version ID. |
| `dataset_versions[].description` | body | `string` | no | Dataset version description. |
