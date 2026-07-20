# Update Conversation Assignee with Front

Updates a conversation assignee in Front.

## Endpoint

- **Method:** `PUT`
- **Path:** `/conversations/:conversation_id/assignee`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [Update Conversation Assignee](https://dev.frontapp.com/reference/update-conversation-assignee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | — |
| `assignee_id` | body | `string` | yes | ID of the teammate to assign the conversation to. |
