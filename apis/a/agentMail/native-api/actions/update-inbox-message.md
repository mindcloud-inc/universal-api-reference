# Update Inbox Message with Agent Mail

Updates a message in a specific AgentMail inbox.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inboxes/{inbox_id}/messages/{message_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Update Inbox Message](https://docs.agentmail.to/api-reference/inboxes/messages/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `message_id` | path | `string` | yes | The AgentMail message ID. |
