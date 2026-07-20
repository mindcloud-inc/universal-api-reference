# Create User with Sunshine Conversations

Creates a new user in Sunshine Conversations.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/:appId/users`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [Create User](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `externalId` | body | `string` | no | Unique external user identifier. |
| `profile` | body | `string` | no | User profile object. |
