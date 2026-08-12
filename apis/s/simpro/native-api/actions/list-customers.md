# List Customers with Simpro

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/customers/`
- **Base URL:** `{buildUrl}/api/v1.0`
- **Official documentation:** [List Customers](https://developer.simprogroup.com/apidoc/?page=e6d0e1c8fc6a4fcf47869df87e04cd88)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Simpro company ID. Single-company builds usually use 0. |
| `columns[]` | query | `array<string>` | no | Columns to return for each customer. |
| `pageSize` | query | `number` | no | Maximum customers per page. |
| `page` | query | `number` | no | Page number. |
| `orderby[]` | query | `array<string>` | no | Sort columns, prefix with - for descending. |
| `limit` | query | `number` | no | Hard limit for number of results. |
