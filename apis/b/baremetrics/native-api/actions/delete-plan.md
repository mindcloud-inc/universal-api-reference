# Delete Plan with Baremetrics

Deletes a plan from Baremetrics.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/:source_id/plans/:oid`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Delete Plan](https://developers.baremetrics.com/reference/delete-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `oid` | path | `string` | yes | — |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
