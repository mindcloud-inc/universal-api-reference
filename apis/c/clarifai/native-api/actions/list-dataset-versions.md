# List Dataset Versions with Clarifai

Retrieves dataset versions from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/me/apps/:appId/datasets/:datasetId/versions`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [List Dataset Versions](https://docs.clarifai.com/create/datasets/manage/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `datasetId` | path | `string` | yes | Clarifai dataset ID. |
