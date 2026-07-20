# List Customer Events with Baremetrics

Retrieves customer events from Baremetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:source_id/customers/:oid/events`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [List Customer Events](https://developers.baremetrics.com/reference/list-customer-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
| `oid` | path | `string` | yes | — |
