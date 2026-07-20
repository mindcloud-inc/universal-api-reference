# List Records with CompanyHub

Retrieves records from a specific CompanyHub table.

## Endpoint

- **Method:** `GET`
- **Path:** `/tables/:tableName`
- **Base URL:** `https://api.companyhub.com/v1`
- **Official documentation:** [List Records](https://companyhub.com/docs/api-documentation#resources)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Exact CompanyHub API table name, for example Contact, Company, Deal, or a custom table name. |
