# List Summary Of Deposits with FDIC

Retrieves summary of deposits data from FDIC.

## Endpoint

- **Method:** `GET`
- **Path:** `/sod`
- **Base URL:** `https://api.fdic.gov/banks`
- **Official documentation:** [List Summary Of Deposits](https://api.fdic.gov/banks/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `string` | no | Elastic Search query string filter for Summary of Deposits records. |
| `fields` | query | `string` | no | Comma-delimited uppercase FDIC fields to include in the response. |
| `agg_by` | query | `string` | no | FDIC aggregate grouping field for Summary of Deposits data. |
| `agg_sum_fields` | query | `string` | no | Comma-delimited fields to sum in FDIC aggregation. |
