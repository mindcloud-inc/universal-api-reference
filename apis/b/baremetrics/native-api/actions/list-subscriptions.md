# List Subscriptions with Baremetrics

Retrieves subscriptions from Baremetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:source_id/subscriptions`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [List Subscriptions](https://developers.baremetrics.com/reference/list-subscriptions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
| `customer_oid` | query | `string` | no | This allows you to return subscriptions for a given customer |
| `order` | query | `string` | no | Allows you to order subscriptions from newest to oldest `desc` or oldest to newest `asc` |
