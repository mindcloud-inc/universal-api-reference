# Get Raw Inbox Message with Agent Mail

Retrieves the raw message from a specific AgentMail inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes/{inbox_id}/messages/{message_id}/raw`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Get Raw Inbox Message](https://docs.agentmail.to/api-reference/inboxes/messages/get-raw)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `message_id` | path | `string` | yes | The AgentMail message ID. |
