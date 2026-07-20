# Change Chat Assignee with Usedesk

Updates a chat assignee in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/changeAssignee`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Change Chat Assignee](https://api.usedocs.com/article/51396)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `number` | yes | Chat ID. |
| `user_id` | body | `number` | yes | ID of the agent you want to assign the chat to. |
