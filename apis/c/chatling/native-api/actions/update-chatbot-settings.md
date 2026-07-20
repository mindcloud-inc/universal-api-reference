# Update Chatbot Settings with Chatling

Updates chatbot settings in Chatling.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/chatbots/:chatbotId`
- **Base URL:** `https://api.chatling.ai/v2`
- **Official documentation:** [Update Chatbot Settings](https://docs.chatling.ai/api-reference/v2/chatbots/update-chatbot-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatbotId` | path | `string` | yes | The chatbot ID. |
| `name` | body | `string` | no | The chatbot name. |
| `visibility` | body | `string` | no | The visibility of the chatbot. |
