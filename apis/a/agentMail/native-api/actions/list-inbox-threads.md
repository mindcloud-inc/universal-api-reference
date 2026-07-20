# List Inbox Threads with Agent Mail

Retrieves threads from a specific AgentMail inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes/{inbox_id}/threads`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [List Inbox Threads](https://docs.agentmail.to/api-reference/inboxes/threads/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
