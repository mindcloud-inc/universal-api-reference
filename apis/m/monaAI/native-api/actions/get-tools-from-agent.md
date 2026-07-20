# Get Tools From Agent with Mona AI

Retrieves tools for an agent from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/database/getToolsFromAgent`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Tools From Agent](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | Mona agent identifier whose tools should be returned. |
