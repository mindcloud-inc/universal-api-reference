# List Inbox Drafts with Agent Mail

Retrieves drafts from a specific AgentMail inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes/{inbox_id}/drafts`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [List Inbox Drafts](https://docs.agentmail.to/api-reference/inboxes/drafts/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
