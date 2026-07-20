# Delete Inbox List Entry with Agent Mail

Deletes an inbox list entry from a specific AgentMail inbox.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/inboxes/{inbox_id}/lists/{direction}/{type}/{entry}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [Delete Inbox List Entry](https://docs.agentmail.to/api-reference/inboxes/lists/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `direction` | path | `string` | yes | List direction: send, receive, or reply. |
| `entry` | path | `string` | yes | Email address or domain entry. |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `type` | path | `string` | yes | List type: allow or block. |
