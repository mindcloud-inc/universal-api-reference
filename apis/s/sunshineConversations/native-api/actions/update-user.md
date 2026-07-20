# Update User with Sunshine Conversations

Updates an existing user in Sunshine Conversations.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/apps/:appId/users/:userIdOrExternalId`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [Update User](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `profile` | body | `string` | no | User profile object. |
| `userIdOrExternalId` | path | `string` | no | User id or external id. |
