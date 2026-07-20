# List WebHooks with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/WebHook/v3/ReadWebHookList`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [List WebHooks](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventType` | body | `string` | no | Optional webhook event type to filter by. |
| `entityIdentifier` | body | `string` | yes | Entity identifier for the webhook subscription, or * for all. |
| `workspaceId` | body | `number` | no | Workspace identifier that owns the webhooks. |
