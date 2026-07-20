# Delete Agent with GPT Chatbot

Deletes an existing agent from GPT Chatbot.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/agent/:uuid/delete`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Delete Agent](https://docs.gptchatbot.it/api-reference/agents/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Agent uuid. |
