# Get Agent with Deskpro

Retrieves an agent record from Deskpro.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/:agentId`
- **Base URL:** `{helpdeskUrl}/api/v2`
- **Official documentation:** [Get Agent](https://www.deskpro.com/developers/api-docs/v2.html#get--api-v2-agents-{id})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `number` | yes | The Deskpro agent id to retrieve. |
