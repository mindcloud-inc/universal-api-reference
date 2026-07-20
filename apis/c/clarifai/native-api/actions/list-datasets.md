# List Datasets with Clarifai

Retrieves datasets from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/me/apps/:appId/datasets`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [List Datasets](https://docs.clarifai.com/create/datasets/manage/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
