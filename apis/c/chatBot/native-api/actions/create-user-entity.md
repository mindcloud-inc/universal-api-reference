# Create User Entity with ChatBot

Creates a new user entity in ChatBot.

## Endpoint

- **Method:** `POST`
- **Path:** `/entities`
- **Base URL:** `https://api.chatbot.com`
- **Official documentation:** [Create User Entity](https://www.chatbot.com/docs/user-entities/#add-new-entity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Entity name. |
| `entries[]` | body | `array<object>` | yes | Entity entries array. |
