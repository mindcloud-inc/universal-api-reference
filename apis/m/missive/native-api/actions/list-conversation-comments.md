# List Conversation Comments with Missive

Retrieves comments from a Missive conversation.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/:id/comments`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [List Conversation Comments](https://missiveapp.com/docs/developers/rest-api/endpoints#list-conversation-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation ID. |
| `limit` | query | `number` | no | Number of comments returned. Default and max 10. |
| `until` | query | `number` | no | Unix timestamp used to paginate with the oldest comment created_at value from the previous page. |
