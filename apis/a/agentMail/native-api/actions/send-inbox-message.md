# Send Inbox Message with Agent Mail

Sends a new message from a specific AgentMail inbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/{inbox_id}/messages/send`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Send Inbox Message](https://docs.agentmail.to/api-reference/inboxes/messages/send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
