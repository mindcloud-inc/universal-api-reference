# Update Chatbot with GPT Chatbot

Updates an existing chatbot in GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/update`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Update Chatbot](https://docs.gptchatbot.it/api-reference/chatbots/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Updated chatbot name. |
| `uuid` | path | `string` | yes | Chatbot uuid. |
