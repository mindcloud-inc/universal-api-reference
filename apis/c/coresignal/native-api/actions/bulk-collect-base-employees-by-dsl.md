# Bulk Collect Base Employees By DSL with Coresignal

Creates a bulk base employee DSL collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/employee_base/es_dsl`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Base Employees By DSL](https://docs.coresignal.com/employee-api/base-employee-api/endpoints/bulk-collect-profiles)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `es_dsl_query` | body | `object` | yes |
