# Reply All To Inbox Message with Agent Mail

Replies to all recipients of an AgentMail message.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/{inbox_id}/messages/{message_id}/reply-all`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Reply All To Inbox Message](https://docs.agentmail.to/api-reference/inboxes/messages/reply-all)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `message_id` | path | `string` | yes | The AgentMail message ID. |
