# List Demographics Summary with FDIC

Retrieves demographic banking data from FDIC.

## Endpoint

- **Method:** `GET`
- **Path:** `/demographics`
- **Base URL:** `https://api.fdic.gov/banks`
- **Official documentation:** [List Demographics Summary](https://api.fdic.gov/banks/docs)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | query | `string` | no | Elastic Search query string filter for demographics records. |
