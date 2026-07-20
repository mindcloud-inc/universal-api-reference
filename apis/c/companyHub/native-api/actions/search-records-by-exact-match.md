# Search Records by Exact Match with CompanyHub

Finds records in CompanyHub by exact field criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/tables/:tableName/search`
- **Base URL:** `https://api.companyhub.com/v1`
- **Official documentation:** [Search Records by Exact Match](https://companyhub.com/docs/api-documentation#howToFilterRecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Exact CompanyHub API table name, for example Contact, Company, Deal, or a custom table name. |
