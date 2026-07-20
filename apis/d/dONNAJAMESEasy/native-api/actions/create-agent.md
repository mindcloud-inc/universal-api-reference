# Create Agent with DONNAJAMES Easy

Creates a new agent for a chatbot in DONNAJAMES Easy.

## Endpoint

- **Method:** `POST`
- **Path:** `chatbot/:uuid/agent/create`
- **Base URL:** `https://app.gpt-trainer.com/api/v1`
- **Official documentation:** [Create Agent](https://guide.gpt-trainer.com/api-reference/agents/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | — |
| `model` | body | `string` | no | — |
| `prompt` | body | `string` | no | — |
| `uuid` | path | `string` | yes | Chatbot uuid |
| `name` | body | `string` | yes | — |
| `type` | body | `string` | yes | — |
| `temperature` | body | `number` | no | — |
| `use_all_sources` | body | `boolean` | no | — |
