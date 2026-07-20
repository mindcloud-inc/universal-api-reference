# Create Record with CompanyHub

Creates a new record in a CompanyHub table.

## Endpoint

- **Method:** `POST`
- **Path:** `/tables/:tableName`
- **Base URL:** `https://api.companyhub.com/v1`
- **Official documentation:** [Create Record](https://companyhub.com/docs/api-documentation#resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Exact CompanyHub API table name, for example Contact, Company, Deal, or a custom table name. |
