# Update User Segments with ChatBot

Updates segments for an existing ChatBot user.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id/segments`
- **Base URL:** `https://api.chatbot.com`
- **Official documentation:** [Update User Segments](https://www.chatbot.com/docs/users/#update-segments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ChatBot user ID. |
| `segmentIds[]` | body | `array<string>` | yes | The segment IDs to replace in the request body array. |
