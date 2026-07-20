# Create User with ChatBot

Creates a new user in ChatBot API.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.chatbot.com`
- **Official documentation:** [Create User](https://www.chatbot.com/docs/users/#create-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | body | `string` | yes | External user identifier. |
| `attributes.default_name` | body | `string` | yes | User display name. |
