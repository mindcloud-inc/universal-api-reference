# Reply To Inbox Message with Agent Mail

Replies to a message from a specific AgentMail inbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/{inbox_id}/messages/{message_id}/reply`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Reply To Inbox Message](https://docs.agentmail.to/api-reference/inboxes/messages/reply)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `message_id` | path | `string` | yes | The AgentMail message ID. |
