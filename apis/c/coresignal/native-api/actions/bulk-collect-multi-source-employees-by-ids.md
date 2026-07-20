# Bulk Collect Multi-source Employees By IDs with Coresignal

Creates a bulk multi-source employee collection request in Coresignal.

## Endpoint

- **Method:** `POST`
- **Path:** `/data_requests/employee_multi_source/ids`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [Bulk Collect Multi-source Employees By IDs](https://docs.coresignal.com/employee-api/multi-source-employee-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes |
