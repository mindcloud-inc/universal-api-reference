# Get Record with CompanyHub

Retrieves a record from a specific CompanyHub table.

## Endpoint

- **Method:** `GET`
- **Path:** `/tables/:tableName/:id`
- **Base URL:** `https://api.companyhub.com/v1`
- **Official documentation:** [Get Record](https://companyhub.com/docs/api-documentation#resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Exact CompanyHub API table name, for example Contact, Company, Deal, or a custom table name. |
| `id` | path | `string` | yes | CompanyHub record ID. |
