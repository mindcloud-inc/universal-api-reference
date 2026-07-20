# List Conversation Drafts with Front

Retrieves a list of conversation drafts from Front.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/:conversation_id/drafts`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [List Conversation Drafts](https://dev.frontapp.com/reference/list-conversation-drafts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | The conversation ID. |
