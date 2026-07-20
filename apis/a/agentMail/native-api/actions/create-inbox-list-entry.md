# Create Inbox List Entry with Agent Mail

Creates an inbox list entry in a specific AgentMail inbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/{inbox_id}/lists/{direction}/{type}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Create Inbox List Entry](https://docs.agentmail.to/api-reference/inboxes/lists/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `direction` | path | `string` | yes | List direction: send, receive, or reply. |
| `entry` | body | `string` | yes | Email address or domain entry to add. |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `reason` | body | `string` | no | Optional reason for the list entry. |
| `type` | path | `string` | yes | List type: allow or block. |
