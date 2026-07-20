# Add segments to User with ChatBot

Adds segments to an existing ChatBot user.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:id/segments`
- **Base URL:** `https://api.chatbot.com`
- **Official documentation:** [Add segments to User](https://www.chatbot.com/docs/users/#add-segments-to-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ChatBot user ID. |
| `segmentIds[]` | body | `array<string>` | yes | The segment IDs to send in the request body array. |
