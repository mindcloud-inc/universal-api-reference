# Show Plan with Baremetrics

Retrieves a plan from Baremetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:source_id/plans/:oid`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Show Plan](https://developers.baremetrics.com/reference/show-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `oid` | path | `string` | yes | — |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
