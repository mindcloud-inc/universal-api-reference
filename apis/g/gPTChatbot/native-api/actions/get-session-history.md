# Get Session History with GPT Chatbot

Retrieves a session's plain-text chat history from GPT Chatbot.

## Endpoint

- **Method:** `GET`
- **Path:** `/session/:uuid/messages/plain-text`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Get Session History](https://docs.gptchatbot.it/api-reference/messages/fetch-message-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Session uuid. |
