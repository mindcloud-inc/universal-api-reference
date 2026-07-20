# List Integration Keys with Sunshine Conversations

Retrieves integration API keys from Sunshine Conversations.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:appId/integrations/:integrationId/keys`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [List Integration Keys](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `integrationId` | path | `string` | no | Integration id. |
