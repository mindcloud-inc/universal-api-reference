# Bulk Collect Base Employees By Filters with Coresignal

Creates a bulk base employee collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/employee_base/filter`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Base Employees By Filters](https://docs.coresignal.com/employee-api/base-employee-api/endpoints/bulk-collect-profiles)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters` | body | `object` | yes |
| `limit` | body | `number` | no |
