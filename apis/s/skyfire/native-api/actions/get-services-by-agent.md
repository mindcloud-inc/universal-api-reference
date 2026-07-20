# Get Services by Agent with Skyfire

Retrieves services for an agent in Skyfire.

## Endpoint

- **Method:** `GET`
- **Path:** `/directory/agents/:agentId/services`
- **Base URL:** `https://api.skyfire.xyz/api/v1`
- **Official documentation:** [Get Services by Agent](https://docs.skyfire.xyz/reference/get-services-by-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | ID of the agent whose services you want to get. |
