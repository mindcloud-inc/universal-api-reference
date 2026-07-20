# Get App Version with mittwald

Retrieves app version from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/apps/:appId/versions/:appVersionId`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get App Version](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | The unique identifier of the app. |
| `appVersionId` | path | `string` | yes | The unique identifier of the app version. |
