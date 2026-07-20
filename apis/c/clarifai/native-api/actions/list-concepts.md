# List Concepts with Clarifai

Retrieves concepts from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/me/apps/:appId/concepts`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [List Concepts](https://docs.clarifai.com/create/concepts/manage/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
