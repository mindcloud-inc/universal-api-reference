# Find Company Employees with Captain Data

Finds company employees in Captain Data by company UID.

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:company_uid/employees`
- **Base URL:** `https://api.captaindata.com/v1`
- **Official documentation:** [Find Company Employees](https://docs.captaindata.com/v1/api/companies/find-employees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_uid` | path | `string` | yes | Captain Data company UID from Find Company or Search Companies. |
| `query` | query | `string` | no | Optional Sales Navigator people-search query for employee filtering. |
| `cursor` | query | `string` | no | Pagination cursor from the X-Pagination-Next response header. |
| `page_size` | query | `number` | no | Captain Data fixed employee-search page size. Leave at the documented default. |
