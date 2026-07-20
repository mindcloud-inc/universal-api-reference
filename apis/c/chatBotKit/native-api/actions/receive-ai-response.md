# Receive AI Response with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/conversation/{conversationId}/receive`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Receive AI Response](https://chatbotkit.com/manuals/conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | The ID of the conversation to receive a response from |
| `functions[]` | body | `array` | no | Functions available during receive |
| `extensions` | body | `object` | no | Extensions for the receive request |
