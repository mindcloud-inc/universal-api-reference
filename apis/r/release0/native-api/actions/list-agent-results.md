# List Agent Results with Release0

Retrieves results for a Release0 agent.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/agents/:agentId/results`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [List Agent Results](https://docs.release0.com/submission/overview)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The agent ID. |
