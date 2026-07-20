# Add Number to Whitelist with Chatvolt AI

Adds a whitelist number in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/agent-whitelist-whatsapp`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Add Number to Whitelist](https://docs.chatvolt.ai/api-reference/endpoint/agents/addWhitelist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | The ID of the agent. |
| `whatsappNumber` | body | `string` | yes | A single WhatsApp number to whitelist. |
