# Get User with Sunshine Conversations

Retrieves a user from Sunshine Conversations.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:appId/users/:userIdOrExternalId`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [Get User](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `userIdOrExternalId` | path | `string` | no | User id or external id. |
