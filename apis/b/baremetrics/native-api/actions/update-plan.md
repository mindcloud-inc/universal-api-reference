# Update Plan with Baremetrics

Updates a plan in Baremetrics.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/:source_id/plans/:plan_oid`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Update Plan](https://developers.baremetrics.com/reference/update-plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `plan_oid` | path | `string` | yes | Your interval plan id |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
| `name` | body | `string` | yes | The new name of this plan |
