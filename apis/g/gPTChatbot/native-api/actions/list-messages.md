# List Messages with GPT Chatbot

Retrieves messages for a session in GPT Chatbot.

## Endpoint

- **Method:** `GET`
- **Path:** `/session/:uuid/messages`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [List Messages](https://docs.gptchatbot.it/api-reference/messages/fetch_multi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Session uuid. |
