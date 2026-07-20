# List Inputs with Clarifai

Retrieves inputs from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/me/apps/:appId/inputs`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [List Inputs](https://docs.clarifai.com/create/inputs/manage/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
