# List Bank Failures with FDIC

Retrieves failed bank records from FDIC.

## Endpoint

- **Method:** `GET`
- **Path:** `/failures`
- **Base URL:** `https://api.fdic.gov/banks`
- **Official documentation:** [List Bank Failures](https://api.fdic.gov/banks/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `string` | no | Elastic Search query string filter for bank failure records, for example FAILYR:2023. |
| `fields` | query | `string` | no | Comma-delimited uppercase FDIC fields to include in the response. |
