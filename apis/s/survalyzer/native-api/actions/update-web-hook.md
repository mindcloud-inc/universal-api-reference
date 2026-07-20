# Update WebHook with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/WebHook/v3/UpdateWebHook`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [Update WebHook](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webHookId` | body | `string` | yes |
| `eventType` | body | `string` | no |
| `entityIdentifier` | body | `string` | no |
| `securityToken` | body | `string` | no |
| `webHookUrl` | body | `string` | no |
| `workspaceId` | body | `number` | no |
