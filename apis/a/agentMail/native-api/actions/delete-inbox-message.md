# Delete Inbox Message with Agent Mail

Permanently deletes a message from a specific AgentMail inbox.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/inboxes/{inbox_id}/messages/{message_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Delete Inbox Message](https://docs.agentmail.to/api-reference/inboxes/messages/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `message_id` | path | `string` | yes | The AgentMail message ID. |
