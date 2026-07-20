# Change Conversation Assignee with Kommunicate

Updates a conversation assignee in Kommunicate.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/ws/group/assignee/change`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Change Conversation Assignee](https://docs.kommunicate.io/docs/api-detail#change-conversation-assignee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | query | `string` | yes | Conversation identifier to update. |
| `assignee` | query | `string` | yes | Human agent email or ID to assign to the conversation. |
| `sendNotifyMessage` | query | `boolean` | no | Whether Kommunicate should send a notification message; defaults to true. |
| `takeOverFromBot` | query | `boolean` | no | Remove bots from the conversation when true. |
| `ofUserId` | query | `string` | yes | Admin or agent user ID to route into the required Of-User-Id header. |
