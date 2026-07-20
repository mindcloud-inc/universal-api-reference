# Create Chatbot with Chatsistant

Creates a new chatbot in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/create`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Create Chatbot](https://docs.chatsistant.com/api-reference/chatbots/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | no | The model name. |
| `name` | body | `string` | no | The chatbot name. |
| `prompt` | body | `string` | no | The chatbot prompt. |
| `temperature` | body | `string` | no | The chatbot temperature. |
| `visibility` | body | `string` | no | The chatbot visibility. |
