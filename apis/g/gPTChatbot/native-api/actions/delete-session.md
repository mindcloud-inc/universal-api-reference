# Delete Session with GPT Chatbot

Deletes an existing session from GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/session/:uuid/delete`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Delete Session](https://docs.gptchatbot.it/api-reference/sessions/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Session uuid. |
