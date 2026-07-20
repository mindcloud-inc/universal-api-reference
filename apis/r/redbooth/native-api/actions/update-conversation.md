# Update Conversation with Redbooth

Updates an existing conversation in Redbooth.

## Endpoint

- **Method:** `PUT`
- **Path:** `/conversations/:id`
- **Base URL:** `https://redbooth.com/api/3`
- **Official documentation:** [Update Conversation](https://redbooth.com/api/api-docs/#page:conversations,header:conversations-conversation-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Redbooth conversation ID |
| `name` | body | `string` | yes | Updated conversation title |
