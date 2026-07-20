# Change Conversation Status with Kommunicate

Updates a conversation status in Kommunicate.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/ws/group/status/change`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Change Conversation Status](https://docs.kommunicate.io/docs/api-detail#change-conversation-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | query | `string` | yes | Conversation identifier to update. |
| `status` | query | `number` | yes | Conversation status code: 0 open, 2 close, 3 spam. |
| `sendNotifyMessage` | query | `boolean` | no | Whether Kommunicate should send a notification message; defaults to true. |
| `ofUserId` | query | `string` | yes | Admin or agent user ID to route into the required Of-User-Id header. |
