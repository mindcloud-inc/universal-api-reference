# List Calls with Phonely

Retrieves calls for a Phonely agent.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/calls/{{agentId}}`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [List Calls](https://docs.phonely.ai/api-reference/endpoint/list-calls)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The ID of the agent whose calls you want to retrieve. |
