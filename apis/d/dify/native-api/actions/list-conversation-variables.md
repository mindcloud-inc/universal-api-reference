# List Conversation Variables with Dify

Retrieves conversation variables from Dify.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/:conversation_id/variables`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [List Conversation Variables](https://docs.dify.ai/api-reference/conversations/list-conversation-variables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID to inspect variables for. |
| `user` | query | `string` | no | User identifier. |
| `last_id` | query | `string` | no | Cursor for the next page of variables. |
| `variable_name` | query | `string` | no | Filter variables by name. |
