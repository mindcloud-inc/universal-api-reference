# List Scripts with PhantomBuster

Retrieves scripts from PhantomBuster.

## Endpoint

- **Method:** `GET`
- **Path:** `/scripts/fetch-all`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [List Scripts](https://hub.phantombuster.com/reference/get_scripts-fetch-all)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch` | query | `string` | no | — |
| `exclude` | query | `list` | no | Accepted values: `modules`, `non-modules`. |
| `org` | query | `string` | no | — |
| `scriptIds` | query | `string` | no | — |
