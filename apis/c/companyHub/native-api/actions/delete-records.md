# Delete Records with CompanyHub

Deletes one or more records from a CompanyHub table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tables/:tableName`
- **Base URL:** `https://api.companyhub.com/v1`
- **Official documentation:** [Delete Records](https://companyhub.com/docs/api-documentation#resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Exact CompanyHub API table name, for example Contact, Company, Deal, or a custom table name. |
