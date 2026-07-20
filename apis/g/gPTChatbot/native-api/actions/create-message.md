# Create Message with GPT Chatbot

Creates a streaming message for a session in GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/session/:uuid/message/stream`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Create Message](https://docs.gptchatbot.it/api-reference/messages/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Message query text. |
| `uuid` | path | `string` | yes | Session uuid. |
