# Update Agent with Chatsistant

Updates an existing chatbot agent in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/agent/:uuid/update`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Update Agent](https://docs.chatsistant.com/api-reference/agents/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The agent description. |
| `model` | body | `string` | no | The agent model. |
| `name` | body | `string` | no | The agent name. |
| `prompt` | body | `string` | no | The agent prompt. |
| `uuid` | path | `string` | no | The agent UUID. |
