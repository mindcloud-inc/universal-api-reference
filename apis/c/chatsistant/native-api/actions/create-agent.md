# Create Agent with Chatsistant

Creates a new chatbot agent in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/chatbot/:uuid/agent/create`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Create Agent](https://docs.chatsistant.com/api-reference/agents/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The agent description. |
| `model` | body | `string` | no | The agent model. |
| `name` | body | `string` | no | The agent name. |
| `prompt` | body | `string` | no | The agent prompt. |
| `temperature` | body | `string` | no | The agent temperature. |
| `type` | body | `string` | no | The agent type. |
| `uuid` | path | `string` | no | The chatbot UUID. |
