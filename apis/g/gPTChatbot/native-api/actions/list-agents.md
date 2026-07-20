# List Agents with GPT Chatbot

Retrieves agents for a chatbot in GPT Chatbot.

## Endpoint

- **Method:** `GET`
- **Path:** `/chatbot/:uuid/agents`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [List Agents](https://docs.gptchatbot.it/api-reference/agents/fetch_multi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Chatbot uuid. |
