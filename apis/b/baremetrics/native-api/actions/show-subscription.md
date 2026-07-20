# Show Subscription with Baremetrics

Retrieves a subscription from Baremetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:source_id/subscriptions/:oid`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Show Subscription](https://developers.baremetrics.com/reference/show-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `oid` | path | `string` | yes | — |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
