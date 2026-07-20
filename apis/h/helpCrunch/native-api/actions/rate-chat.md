# Rate Chat with HelpCrunch

Updates a chat's rating in HelpCrunch.

## Endpoint

- **Method:** `PUT`
- **Path:** `/chats/rate`
- **Base URL:** `https://api.helpcrunch.com/v1`
- **Official documentation:** [Rate Chat](https://docs.helpcrunch.com/en/rest-api-v1/chat-rating-rest-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | yes |
| `rating` | body | `string` | yes |
