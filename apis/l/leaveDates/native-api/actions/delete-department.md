# Delete Department with Leave Dates

Deletes an existing department from Leave Dates.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/departments/:id`
- **Base URL:** `https://api.leavedates.com`
- **Official documentation:** [Delete Department](https://api.leavedates.com/documentation#/Company/delete_departments__id_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `company_id` | body | `string` | yes |
