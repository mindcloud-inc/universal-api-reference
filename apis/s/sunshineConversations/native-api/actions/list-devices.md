# List Devices with Sunshine Conversations

Retrieves a user's devices from Sunshine Conversations.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:appId/users/:userIdOrExternalId/devices`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [List Devices](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `userIdOrExternalId` | path | `string` | no | User id or external id. |
