# List Clients with Sunshine Conversations

Retrieves a user's clients from Sunshine Conversations.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:appId/users/:userIdOrExternalId/clients`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [List Clients](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `userIdOrExternalId` | path | `string` | no | User id or external id. |
