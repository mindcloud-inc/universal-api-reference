# Create Inbox Draft with Agent Mail

Creates a new draft in a specific AgentMail inbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/{inbox_id}/drafts`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Create Inbox Draft](https://docs.agentmail.to/api-reference/inboxes/drafts/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
