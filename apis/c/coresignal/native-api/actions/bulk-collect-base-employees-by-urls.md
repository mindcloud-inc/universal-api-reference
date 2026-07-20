# Bulk Collect Base Employees By URLs with Coresignal

Creates a bulk base employee URL collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/employee_base/urls`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Base Employees By URLs](https://docs.coresignal.com/employee-api/base-employee-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes |
