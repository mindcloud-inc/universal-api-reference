# Update Department with Leave Dates

Updates an existing department in Leave Dates.

## Endpoint

- **Method:** `PUT`
- **Path:** `/departments/:id`
- **Base URL:** `https://api.leavedates.com`
- **Official documentation:** [Update Department](https://api.leavedates.com/documentation#/Company/put_departments__id_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `company_id` | body | `string` | yes |
| `name` | body | `string` | yes |
