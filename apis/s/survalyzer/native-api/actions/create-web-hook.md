# Create WebHook with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/WebHook/v3/CreateWebHook`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [Create WebHook](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventType` | body | `string` | no |
| `entityIdentifier` | body | `string` | yes |
| `securityToken` | body | `string` | no |
| `webHookUrl` | body | `string` | yes |
| `workspaceId` | body | `number` | no |
