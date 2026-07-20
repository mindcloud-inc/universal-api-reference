# Delete Inbox Draft with Agent Mail

Deletes a draft from a specific AgentMail inbox.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/inboxes/{inbox_id}/drafts/{draft_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Delete Inbox Draft](https://docs.agentmail.to/api-reference/inboxes/drafts/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draft_id` | path | `string` | yes | The AgentMail draft ID. |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
