# Delete Inbox Thread with Agent Mail

Deletes a thread from AgentMail, or permanently deletes trashed threads.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/inboxes/{inbox_id}/threads/{thread_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Delete Inbox Thread](https://docs.agentmail.to/api-reference/inboxes/threads/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `thread_id` | path | `string` | yes | The AgentMail thread ID. |
