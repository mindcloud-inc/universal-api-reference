# Create Chat Completion with CometAPI

Creates a chat completion in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/completions`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Create Chat Completion](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Conversation messages in OpenAI chat format. |
| `model` | body | `string` | yes | Model ID to use for the chat completion. |
