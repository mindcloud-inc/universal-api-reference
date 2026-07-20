# Get Agent Last Known Position with AntsRoute

Retrieves an agent's last known position in AntsRoute.

## Endpoint

- **Method:** `GET`
- **Path:** `/capi/agent/:agentEmail/last-known-position`
- **Base URL:** `https://app.antsroute.com`
- **Official documentation:** [Get Agent Last Known Position](https://app.antsroute.com/doc-api/index.html#/Agent/getLastKnownPosition)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentEmail` | path | `string` | yes |
