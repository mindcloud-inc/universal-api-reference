# Delete Number from Whitelist with Chatvolt AI

Deletes a whitelist number from Chatvolt AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/agent-whitelist-whatsapp/{id}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Delete Number from Whitelist](https://docs.chatvolt.ai/api-reference/endpoint/agents/deleteWhitelist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the agent. |
| `whatsappNumber` | body | `string` | yes | The WhatsApp number to be removed from the whitelist. |
