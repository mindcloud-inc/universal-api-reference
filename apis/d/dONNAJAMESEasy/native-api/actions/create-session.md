# Create Session with DONNAJAMES Easy

Creates a new session for a chatbot in DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `chatbot/:uuid/session/create`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Create Session](https://guide.gpt-trainer.com/api-reference/sessions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Chatbot uuid |
| `initial_variables` | body | `object` | no | — |
