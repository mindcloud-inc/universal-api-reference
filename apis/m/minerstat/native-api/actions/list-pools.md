# List Pools with Minerstat

Retrieves mining pools from the Minerstat catalog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/pools`
- **Base URL:** `https://api.minerstat.com`
- **Official documentation:** [List Pools](https://api.minerstat.com/docs-pools/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `coin` | query | `string` | no | Payout coin symbol like ETH. |
| `type` | query | `string` | no | Pool category like multipool. |
