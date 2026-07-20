# Add Department with Leave Dates

Creates a new department in Leave Dates.

## Endpoint

- **Method:** `POST`
- **Path:** `/departments`
- **Base URL:** `https://api.leavedates.com`
- **Official documentation:** [Add Department](https://api.leavedates.com/documentation#/Company/post_departments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | body | `string` | yes |
| `name` | body | `string` | yes |
