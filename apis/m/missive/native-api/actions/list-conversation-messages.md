# List Conversation Messages with Missive

Retrieves messages from a Missive conversation.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/:id/messages`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [List Conversation Messages](https://missiveapp.com/docs/developers/rest-api/endpoints#list-conversation-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation ID. |
| `limit` | query | `number` | no | Number of messages returned. Default and max 10. |
| `until` | query | `number` | no | Unix timestamp used to paginate with the oldest message delivered_at value from the previous page. |
