# Update Record with CompanyHub

Updates an existing record in a CompanyHub table.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tables/:tableName/:id`
- **Base URL:** `https://api.companyhub.com/v1`
- **Official documentation:** [Update Record](https://companyhub.com/docs/api-documentation#resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Exact CompanyHub API table name, for example Contact, Company, Deal, or a custom table name. |
| `id` | path | `string` | yes | CompanyHub record ID. |
