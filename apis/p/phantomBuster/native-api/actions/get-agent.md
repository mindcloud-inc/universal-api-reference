# Get Agent with PhantomBuster

Retrieves an agent from PhantomBuster.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/fetch`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Get Agent](https://hub.phantombuster.com/reference/get_agents-fetch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The PhantomBuster agent ID to fetch. |
| `withAgentObject` | query | `string` | no | — |
| `withCode` | query | `string` | no | — |
| `withManifest` | query | `string` | no | — |
| `withSlaves` | query | `string` | no | — |
| `withSubSlaves` | query | `string` | no | — |
