# Get Extension Chargability with mittwald

Retrieves whether an extension is chargeable from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/extensions/:extensionId/contexts/:contextId/chargability`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Extension Chargability](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contextId` | path | `string` | yes | The unique identifier of the extension context. |
| `extensionId` | path | `string` | yes | The unique identifier of the extension. |
