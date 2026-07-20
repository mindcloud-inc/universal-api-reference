# List Financial Institutions with FDIC

Retrieves financial institutions from FDIC.

## Endpoint

- **Method:** `GET`
- **Path:** `/institutions`
- **Base URL:** `https://api.fdic.gov/banks`
- **Official documentation:** [List Financial Institutions](https://api.fdic.gov/banks/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `string` | no | Elastic Search query string filter, for example STALP:IA AND ACTIVE:1. |
| `search` | query | `string` | no | Flexible text search against institution names, for example NAME:Island. |
| `fields` | query | `string` | no | Comma-delimited uppercase FDIC fields to include in the response. |
