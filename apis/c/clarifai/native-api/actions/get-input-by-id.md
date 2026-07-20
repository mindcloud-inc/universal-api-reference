# Get Input By ID with Clarifai

Retrieves an input from Clarifai.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/users/me/apps/:appId/inputs/:inputId`
- **Base URL:** `https://api.clarifai.com`
- **Official documentation:** [Get Input By ID](https://docs.clarifai.com/create/inputs/manage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Clarifai app ID. |
| `inputId` | path | `string` | yes | Clarifai input ID. |
