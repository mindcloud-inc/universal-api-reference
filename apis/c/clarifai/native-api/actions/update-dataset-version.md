# Update Dataset Version with Clarifai

Updates an existing dataset version in Clarifai.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/users/{userId}/apps/{{appId}}/datasets/{{datasetId}}/versions`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Update Dataset Version](https://docs.clarifai.com/create/datasets/manage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Clarifai app ID. |
| `datasetId` | path | `string` | no | Clarifai dataset ID. |
