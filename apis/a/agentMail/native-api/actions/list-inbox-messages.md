# List Inbox Messages with Agent Mail

Retrieves messages from a specific AgentMail inbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes/{inbox_id}/messages`
- **Base URL:** `https://api.agentmail.to/v0`
- **Official documentation:** [List Inbox Messages](https://docs.agentmail.to/api-reference/inboxes/messages/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | path | `string` | yes | The AgentMail inbox ID. |
