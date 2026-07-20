# List App Versions with mittwald

Retrieves app versions from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/apps/:appId/versions`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List App Versions](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | The app ID. |
