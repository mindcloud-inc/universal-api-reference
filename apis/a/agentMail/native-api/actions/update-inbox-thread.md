# Update Inbox Thread with Agent Mail

Updates a thread in a specific AgentMail inbox.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inboxes/{inbox_id}/threads/{thread_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Update Inbox Thread](https://docs.agentmail.to/api-reference/inboxes/threads/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `thread_id` | path | `string` | yes | The AgentMail thread ID. |
