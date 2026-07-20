# List Containers with PhantomBuster

Retrieves containers from PhantomBuster.

## Endpoint

- **Method:** `GET`
- **Path:** `/containers/fetch-all`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [List Containers](https://hub.phantombuster.com/reference/get_containers-fetch-all)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | query | `string` | yes | Id of the agent to fetch containers from. |
| `beforeEndedAt` | query | `string` | no | — |
| `mode` | query | `list` | no | Accepted values: `all`, `finalized`. |
| `withRuntimeEvents` | query | `string` | no | — |
