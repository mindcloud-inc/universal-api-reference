# List Historical Aggregate Data with FDIC

Retrieves historical aggregate banking data from FDIC.

## Endpoint

- **Method:** `GET`
- **Path:** `/summary`
- **Base URL:** `https://api.fdic.gov/banks`
- **Official documentation:** [List Historical Aggregate Data](https://api.fdic.gov/banks/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `string` | no | Elastic Search query string filter for historical aggregate data. |
| `fields` | query | `string` | no | Comma-delimited uppercase FDIC fields to include in the response. |
| `agg_by` | query | `string` | no | FDIC aggregate grouping field for summary data. |
| `agg_sum_fields` | query | `string` | no | Comma-delimited fields to sum in FDIC aggregation. |
