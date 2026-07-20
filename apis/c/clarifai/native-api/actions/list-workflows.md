# List Workflows with Clarifai

Retrieves workflows from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/me/apps/:appId/workflows`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [List Workflows](https://docs.clarifai.com/create/workflows/manage/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `search` | query | `string` | no | Search term for workflow ID. |
