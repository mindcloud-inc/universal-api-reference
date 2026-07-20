# Get Inbox Thread with Agent Mail

Retrieves a thread from a specific AgentMail inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes/{inbox_id}/threads/{thread_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Get Inbox Thread](https://docs.agentmail.to/api-reference/inboxes/threads/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `thread_id` | path | `string` | yes | The AgentMail thread ID. |
