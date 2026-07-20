# Get Server Storage Space Statistics with mittwald

Retrieves server storage statistics from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/servers/:serverId/storage-space-statistics`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Server Storage Space Statistics](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serverId` | path | `string` | yes | The unique identifier of the server. |
