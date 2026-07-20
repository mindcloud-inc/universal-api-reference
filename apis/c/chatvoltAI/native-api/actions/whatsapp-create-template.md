# Create Meta Template with Chatvolt AI

Creates a meta Template in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/templates`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create Meta Template](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/create-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | ID of the agent. |
| `name` | body | `string` | yes | Name of the template. |
| `category` | body | `string` | yes | Category of the template. |
| `language` | body | `string` | yes | Language code (e.g., "en_US"). |
| `components[]` | body | `array<object>` | yes | Template components (header, body, footer, buttons). |
