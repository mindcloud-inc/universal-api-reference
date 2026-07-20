# Get Script with PhantomBuster

Retrieves a script from PhantomBuster.

## Endpoint

- **Method:** `GET`
- **Path:** `/scripts/fetch`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Get Script](https://hub.phantombuster.com/reference/get_scripts-fetch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch` | query | `string` | no | — |
| `environment` | query | `list` | no | Accepted values: `release`, `staging`. |
| `id` | query | `string` | yes | The PhantomBuster script ID to fetch. |
| `withCode` | query | `list` | no | Accepted values: `release`, `staging`. |
