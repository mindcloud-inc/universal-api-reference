# Delete User with Sunshine Conversations

Deletes a user, clients, and conversation history from Sunshine Conversations.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/apps/:appId/users/:userIdOrExternalId`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [Delete User](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `userIdOrExternalId` | path | `string` | no | User id or external id. |
