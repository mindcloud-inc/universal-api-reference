# Get Script Code with PhantomBuster

Retrieves script code from PhantomBuster.

## Endpoint

- **Method:** `GET`
- **Path:** `/scripts/code`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Get Script Code](https://hub.phantombuster.com/reference/get_scripts-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch` | query | `string` | no | — |
| `environment` | query | `list` | no | Accepted values: `release`, `staging`. |
| `org` | query | `string` | no | — |
| `script` | query | `string` | yes | The PhantomBuster script identifier whose code you want. |
