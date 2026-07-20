# Get Inbox Message Attachment with Agent Mail

Retrieves a message attachment from a specific AgentMail inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes/{inbox_id}/messages/{message_id}/attachments/{attachment_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Get Inbox Message Attachment](https://docs.agentmail.to/api-reference/inboxes/messages/get-attachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachment_id` | path | `string` | yes | The AgentMail attachment ID. |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `message_id` | path | `string` | yes | The AgentMail message ID. |
