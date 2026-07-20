# Get Conversation Reporting Events with OneHash

Retrieves conversation reporting events from OneHash.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/accounts/:accountId/conversations/:conversationId/reporting_events`
- **Base URL:** `https://chat.onehash.ai`
- **Official documentation:** [Get Conversation Reporting Events](https://developers.chatwoot.com/api-reference/conversations/conversation-reporting-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | no | The OneHash account ID. |
| `conversationId` | path | `string` | no | The conversation ID. |
