# Create Bot Session with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/bot/{botId}/session/create`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Create Bot Session](https://chatbotkit.com/manuals/bot-sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The ID of the bot to create a session for |
| `durationInSeconds` | body | `number` | no | Session duration in seconds |
| `messages[]` | body | `array` | no | Messages used to initialize the session |
| `meta` | body | `object` | no | Metadata for the session |
