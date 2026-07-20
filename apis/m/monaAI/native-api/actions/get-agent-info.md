# Get Agent Info with Mona AI

Retrieves a specific agent from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/agent/getAgentInfo`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Agent Info](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | Mona agent identifier to retrieve. |
| `permission` | body | `string` | yes | Mona permission string required by this agent lookup endpoint. |
