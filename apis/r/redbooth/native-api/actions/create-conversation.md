# Create Conversation with Redbooth

Creates a new conversation in Redbooth.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations`
- **Base URL:** `https://redbooth.com/api/3`
- **Official documentation:** [Create Conversation](https://redbooth.com/api/api-docs/#page:conversations,header:conversations-conversation-list-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Conversation title |
| `project_id` | body | `number` | yes | Parent project ID |
