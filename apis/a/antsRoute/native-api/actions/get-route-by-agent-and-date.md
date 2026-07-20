# Get Route by Agent and Date with AntsRoute

Retrieves an AntsRoute route by agent and date.

## Endpoint

- **Method:** `GET`
- **Path:** `/capi/route/:agentEmail/:date`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [Get Route by Agent and Date](https://app.antsroute.com/doc-api/index.html#/Route/getRouteByAgentEmailAndDate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentEmail` | path | `string` | yes | — |
| `date` | path | `string` | yes | format: yyyy-MM-dd |
