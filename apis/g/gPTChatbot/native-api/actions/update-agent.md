# Update Agent with GPT Chatbot

Updates an existing agent in GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/agent/:uuid/update`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Update Agent](https://docs.gptchatbot.it/api-reference/agents/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Updated agent name. |
| `uuid` | path | `string` | yes | Agent uuid. |
