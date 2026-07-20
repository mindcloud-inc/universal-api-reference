# Get Next Suggested Questions with Dify

Retrieves suggested questions from Dify.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/:message_id/suggested`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Get Next Suggested Questions](https://docs.dify.ai/api-reference/chats/get-next-suggested-questions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | path | `string` | yes | Message ID to fetch suggestions for. |
| `user` | query | `string` | yes | User identifier. |
