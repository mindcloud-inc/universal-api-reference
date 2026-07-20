# List Conversation Posts with Missive

Retrieves posts from a Missive conversation.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/:id/posts`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [List Conversation Posts](https://missiveapp.com/docs/developers/rest-api/endpoints#list-conversation-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation ID. |
| `limit` | query | `number` | no | Number of posts returned. Default and max 10. |
| `until` | query | `number` | no | Unix timestamp used to paginate with the oldest post created_at value from the previous page. |
