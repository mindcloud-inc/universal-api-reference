# Get Inbox Draft Attachment with Agent Mail

Retrieves a draft attachment from a specific AgentMail inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes/{inbox_id}/drafts/{draft_id}/attachments/{attachment_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Get Inbox Draft Attachment](https://docs.agentmail.to/api-reference/inboxes/drafts/get-attachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment_id` | path | `string` | yes | The AgentMail attachment ID. |
| `draft_id` | path | `string` | yes | The AgentMail draft ID. |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
