# Update User Entity with ChatBot

Updates an existing user entity in ChatBot.

## Endpoint

- **Method:** `PUT`
- **Path:** `/entities/:ID`
- **Base URL:** `https://api.chatbot.com`
- **Official documentation:** [Update User Entity](https://www.chatbot.com/docs/user-entities/#update-entity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | path | `string` | yes | ChatBot entity id. |
| `name` | body | `string` | yes | Updated entity name. |
| `entries[]` | body | `array<object>` | yes | Updated entity entries array. |
