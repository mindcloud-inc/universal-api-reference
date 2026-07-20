# Ban or Unban User with ChatBot

Updates the ban status of a ChatBot user.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id/ban`
- **Base URL:** `https://api.chatbot.com`
- **Official documentation:** [Ban or Unban User](https://www.chatbot.com/docs/users/#ban-or-unban-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ChatBot user id. |
| `banned` | body | `boolean` | yes | Whether the user should be banned. |
