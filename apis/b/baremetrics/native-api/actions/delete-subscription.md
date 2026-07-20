# Delete Subscription with Baremetrics

Deletes a subscription from Baremetrics.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/:source_id/subscriptions/:oid`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Delete Subscription](https://developers.baremetrics.com/reference/delete-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `oid` | path | `string` | yes | — |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
