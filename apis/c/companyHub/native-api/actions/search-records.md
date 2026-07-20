# Search Records with CompanyHub

Finds records in CompanyHub by broad text search.

## Endpoint

- **Method:** `GET`
- **Path:** `/tables/:tableName`
- **Base URL:** `https://api.companyhub.com/v1`
- **Official documentation:** [Search Records](https://companyhub.com/docs/api-documentation#howToFilterRecords)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Exact CompanyHub API table name, for example Contact, Company, Deal, or a custom table name. |
| `searchText` | query | `string` | yes | Text to search across the selected table. |
