# List Plans with Baremetrics

Retrieves plans from Baremetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:source_id/plans`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [List Plans](https://developers.baremetrics.com/reference/list-plans)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Allows you to search based on the name or oid fields |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
