# Update Conversation Variable with Dify

Updates an existing conversation variable in Dify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/conversations/:conversation_id/variables/:variable_id`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Update Conversation Variable](https://docs.dify.ai/api-reference/conversations/update-conversation-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID that owns the variable. |
| `variable_id` | path | `string` | yes | Variable ID to update. |
| `value` | body | `object` | yes | New value for the variable. |
| `user` | body | `string` | no | User identifier. |
