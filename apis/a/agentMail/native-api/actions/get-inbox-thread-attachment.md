# Get Inbox Thread Attachment with Agent Mail

Retrieves a thread attachment from a specific AgentMail inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes/{inbox_id}/threads/{thread_id}/attachments/{attachment_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Get Inbox Thread Attachment](https://docs.agentmail.to/api-reference/inboxes/threads/get-attachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment_id` | path | `string` | yes | The AgentMail attachment ID. |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `thread_id` | path | `string` | yes | The AgentMail thread ID. |
