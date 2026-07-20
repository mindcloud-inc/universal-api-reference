# Get Agent with Chatvolt AI

Retrieves an agent from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/{id}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Get Agent](https://docs.chatvolt.ai/api-reference/endpoint/agents/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Agent ID or its handle (unique identifier preceded by '@', e.g., '@my-agent'). |
