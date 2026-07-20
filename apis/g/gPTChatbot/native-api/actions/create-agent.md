# Create Agent with GPT Chatbot

Creates an agent for a chatbot in GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/agent/create`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Create Agent](https://docs.gptchatbot.it/api-reference/agents/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Chatbot uuid. |
| `name` | body | `string` | yes | Agent name. |
| `type` | body | `string` | yes | Agent type. |
| `prompt` | body | `string` | no | Agent system prompt. |
| `description` | body | `string` | yes | Agent description. |
