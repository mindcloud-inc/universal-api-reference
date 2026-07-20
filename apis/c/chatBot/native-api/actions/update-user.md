# Update User with ChatBot

Updates an existing user in ChatBot API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id`
- **Base URL:** `https://api.chatbot.com`
- **Official documentation:** [Update User](https://www.chatbot.com/docs/users/#update-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ChatBot user id. |
| `attributes.default_name` | body | `string` | yes | Updated user display name. |
