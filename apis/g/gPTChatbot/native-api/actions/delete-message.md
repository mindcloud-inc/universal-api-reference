# Delete Message with GPT Chatbot

Deletes an existing message from GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/message/:uuid/delete`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Delete Message](https://docs.gptchatbot.it/api-reference/messages/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Message uuid. |
