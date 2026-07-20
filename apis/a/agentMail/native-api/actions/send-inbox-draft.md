# Send Inbox Draft with Agent Mail

Sends a draft from a specific AgentMail inbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/{inbox_id}/drafts/{draft_id}/send`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Send Inbox Draft](https://docs.agentmail.to/api-reference/inboxes/drafts/send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draft_id` | path | `string` | yes | The AgentMail draft ID. |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
