# Create Web Tool with Hamsa

Creates a new web tool in Hamsa.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/voice-agents/web-tool`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Create Web Tool](https://docs.tryhamsa.com/api-reference/endpoint/v2/create-web-tool)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `async` | body | `boolean` | yes |
| `async` | body | `boolean` | yes |
| `collectionId` | body | `string` | no |
| `collectionId` | body | `string` | no |
| `description` | body | `string` | yes |
| `description` | body | `string` | yes |
| `messages[]` | body | `array<object>` | yes |
| `messages[]` | body | `array<object>` | yes |
| `messages[].content` | body | `string` | yes |
| `messages[].content` | body | `string` | yes |
| `messages[].type` | body | `string` | yes |
| `messages[].type` | body | `string` | yes |
| `name` | body | `string` | yes |
| `params` | body | `object` | yes |
| `params` | body | `object` | yes |
| `toolSettings` | body | `object` | yes |
| `toolSettings` | body | `object` | yes |
| `toolSettings.authToken` | body | `string` | no |
| `toolSettings.authToken` | body | `string` | no |
| `toolSettings.httpHeaders` | body | `object` | no |
| `toolSettings.httpHeaders` | body | `object` | no |
| `toolSettings.methodType` | body | `string` | yes |
| `toolSettings.methodType` | body | `string` | yes |
| `toolSettings.pathParameters` | body | `object` | no |
| `toolSettings.pathParameters` | body | `object` | no |
| `toolSettings.serverUrl` | body | `string` | yes |
| `toolSettings.serverUrl` | body | `string` | yes |
| `toolSettings.timeout` | body | `number` | no |
| `toolSettings.timeout` | body | `number` | no |
| `type` | body | `string` | yes |
