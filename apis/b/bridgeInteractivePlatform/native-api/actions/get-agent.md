# Get agent with Bridge Interactive Platform

Retrieves an agent from Bridge Interactive Platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/:dataset/agents/:agentId`
- **Base URL:** `https://api.bridgedataoutput.com/api/v2`
- **Official documentation:** [Get agent](https://bridgedataoutput.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | Bridge agent identifier from the REST agents feed. |
| `dataset` | path | `string` | yes | Bridge dataset code. This tenant was validated against dataset test. |
