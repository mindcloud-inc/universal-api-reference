# Mark Chat As Read By Agent with HelpCrunch

Marks a chat as read by an agent in HelpCrunch.

## Endpoint

- **Method:** `PUT`
- **Path:** `/chats/readByAgent`
- **Base URL:** `https://api.helpcrunch.com/v1`
- **Official documentation:** [Mark Chat As Read By Agent](https://docs.helpcrunch.com/en/rest-api-v1/read-chat-rest-api-1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | yes |
| `read` | body | `boolean` | yes |
