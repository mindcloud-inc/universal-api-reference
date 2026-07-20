# Location Request with Chatvolt AI

Sends a location request through Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/interactive/location-request`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Location Request](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/location-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | The ID of the agent. |
| `conversationId` | body | `string` | yes | The ID of the conversation. |
| `body_text` | body | `string` | yes | Text explaining why the location is needed. |
