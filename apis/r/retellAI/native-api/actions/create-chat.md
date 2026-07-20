# Create Chat with Retell AI

Creates a chat in Retell AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/create-chat`
- **Base URL:** `https://api.retellai.com`
- **Official documentation:** [Create Chat](https://docs.retellai.com/api-references/create-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | yes | The chat agent to use for the call. |
| `agent_version` | body | `number` | no | The version of the chat agent to use for the chat. If not provided, will default to latest version. |
| `metadata` | body | `object` | no | An arbitrary object for storage purpose only. You can put anything here like your internal customer id associated with the chat. Not used for processing. You can later get this field from the chat object. |
| `retell_llm_dynamic_variables` | body | `object` | no | Add optional dynamic variables in key value pairs of string that injects into your Response Engine prompt and tool description. Only applicable for Response Engine. |
