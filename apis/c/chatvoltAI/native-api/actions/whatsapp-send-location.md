# Send Location with Chatvolt AI

Sends a location message through Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/interactive/send-location`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Send Location](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/send-location)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | The ID of the agent. |
| `conversationId` | body | `string` | yes | The ID of the conversation. |
| `latitude` | body | `string` | yes | Latitude of the location. |
| `longitude` | body | `string` | yes | Longitude of the location. |
| `name` | body | `string` | yes | Name of the place. |
| `address` | body | `string` | yes | Address of the place. |
