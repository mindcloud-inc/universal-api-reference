# Get Agent Result with Mona AI

Retrieves an agent result from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/agent/getAgentResult`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Agent Result](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | Mona agent identifier for the result lookup. |
| `resultId` | body | `string` | yes | Mona agent result identifier to retrieve. |
