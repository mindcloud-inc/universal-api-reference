# Update Inbox with Agent Mail

Updates an existing inbox in AgentMail.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inboxes/{inbox_id}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Update Inbox](https://docs.agentmail.to/api-reference/inboxes/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `display_name` | body | `string` | yes | Display name for the inbox. |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
