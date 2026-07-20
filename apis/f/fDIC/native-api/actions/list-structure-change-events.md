# List Structure Change Events with FDIC

Retrieves structure change events from FDIC.

## Endpoint

- **Method:** `GET`
- **Path:** `/history`
- **Base URL:** `https://api.fdic.gov/banks`
- **Official documentation:** [List Structure Change Events](https://api.fdic.gov/banks/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `string` | no | Elastic Search query string filter for structure change events. |
| `search` | query | `string` | no | Flexible text search against history records. |
| `fields` | query | `string` | no | Comma-delimited uppercase FDIC fields to include in the response. |
