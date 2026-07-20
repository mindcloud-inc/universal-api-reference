# List Inbox List Entries with Agent Mail

Retrieves inbox list entries from a specific AgentMail inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes/{inbox_id}/lists/{direction}/{type}`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [List Inbox List Entries](https://docs.agentmail.to/api-reference/inboxes/lists/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `direction` | path | `string` | yes | List direction: send, receive, or reply. |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
| `type` | path | `string` | yes | List type: allow or block. |
