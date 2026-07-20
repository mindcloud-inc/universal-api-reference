# Update Number in Whitelist with Chatvolt AI

Updates a whitelist number in Chatvolt AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/agent-whitelist-whatsapp/{id}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Update Number in Whitelist](https://docs.chatvolt.ai/api-reference/endpoint/agents/patchWhitelist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the agent. |
| `oldWhatsappNumber` | body | `string` | yes | The current WhatsApp number in the whitelist. |
| `newWhatsappNumber` | body | `string` | yes | The new WhatsApp number to replace the old one. |
