# List Conversation Messages with Front

Retrieves a list of conversation messages from Front.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/:conversation_id/messages`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [List Conversation Messages](https://dev.frontapp.com/reference/list-conversation-messages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | — |
| `sort_by` | query | `list` | no | Accepted values: `created_at`. |
| `sort_order` | query | `list` | no | Accepted values: `asc`, `desc`. |
