# Create Session with GPT Chatbot

Creates a session for a chatbot in GPT Chatbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/session/create`
- **Base URL:** `https://app.gptchatbot.it/api/v1`
- **Official documentation:** [Create Session](https://docs.gptchatbot.it/api-reference/sessions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `initial_variables` | body | `object` | no | Initial flat object of variables to store with the session. |
| `uuid` | path | `string` | yes | Chatbot uuid. |
