# Update Inbox Draft with Agent Mail

Updates a draft in a specific AgentMail inbox.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inboxes/{inbox_id}/drafts/{draft_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Update Inbox Draft](https://docs.agentmail.to/api-reference/inboxes/drafts/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draft_id` | path | `string` | yes | The AgentMail draft ID. |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
