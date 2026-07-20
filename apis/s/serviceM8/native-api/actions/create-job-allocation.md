# Create Job Allocation with ServiceM8

## Endpoint

- **Method:** `POST`
- **Path:** `/api_1.0/joballocation.json`
- **Base URL:** `https://api.servicem8.com`
- **Official documentation:** [Create Job Allocation](https://developer.servicem8.com/reference/createjoballocations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_uuid` | body | `string` | no | — |
| `staff_uuid` | body | `string` | no | — |
| `allocation_date` | body | `date` | no | — |
| `allocation_window_uuid` | body | `string` | yes | Required ServiceM8 allocation window UUID. Retrieve this from the Allocation Windows resource configured in the connected ServiceM8 tenant. |
| `sort_priority` | body | `string` | no | — |
| `allocated_by_staff_uuid` | body | `string` | no | — |
| `allocated_timestamp` | body | `date` | no | — |
| `expiry_timestamp` | body | `date` | no | — |
| `read_timestamp` | body | `date` | no | — |
| `completion_timestamp` | body | `date` | no | — |
| `uuid` | body | `string` | no | — |
