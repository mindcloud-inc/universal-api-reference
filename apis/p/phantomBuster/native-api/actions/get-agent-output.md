# Get Agent Output with PhantomBuster

Retrieves agent output from PhantomBuster.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/fetch-output`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Get Agent Output](https://hub.phantombuster.com/reference/get_agents-fetch-output)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromOutputPos` | query | `number` | no | — |
| `id` | query | `string` | yes | The PhantomBuster agent ID whose latest output you want. |
| `prevContainerId` | query | `string` | no | — |
| `prevRuntimeEventIndex` | query | `number` | no | — |
| `prevStatus` | query | `list` | no | Accepted values: `finished`, `launch error`, `never launched`, `running`, `starting`, `unknown`. |
