# List Sessions with GPT Chatbot

Retrieves sessions for a chatbot in GPT Chatbot.

## Endpoint

- **Method:** `GET`
- **Path:** `/chatbot/:uuid/sessions`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [List Sessions](https://docs.gptchatbot.it/api-reference/sessions/fetch_multi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_timestamp` | query | `date` | no | Filter sessions created before this timestamp (inclusive), in ISO 8601 UTC. |
| `start_timestamp` | query | `date` | no | Filter sessions created after this timestamp (inclusive), in ISO 8601 UTC. |
| `uuid` | path | `string` | yes | Chatbot uuid. |
