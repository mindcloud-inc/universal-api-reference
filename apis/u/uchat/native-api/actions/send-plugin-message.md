# Send Plugin Message with Uchat

Sends an array-wrapped message payload to a Uchat plugin.

## Endpoint

- **Method:** `POST`
- **Path:** `/plugin/:pluginId`
- **Base URL:** `https://api.uchat.io`
- **Official documentation:** [Send Plugin Message](https://uchat.io/doc/2.5/%EC%84%9C%EB%B2%84-API)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `User-Agent` | `uchat_api_client_v1` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload[]` | body | `array` | yes | Array-wrapped JSON payload passed to the target Uchat plugin. |
| `pluginId` | path | `string` | yes | Installed Uchat plugin identifier from the /plugin/{pluginId} path. |
