# Update Employment with Leave Dates

Updates an existing employment in Leave Dates.

## Endpoint

- **Method:** `PUT`
- **Path:** `/employments/:id`
- **Base URL:** `https://api.leavedates.com`
- **Official documentation:** [Update Employment](https://api.leavedates.com/documentation#/Employment/put_employments__id_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `company_id` | body | `string` | yes |
| `full_name` | body | `string` | yes |
| `email` | body | `string` | yes |
| `timezone` | body | `string` | yes |
| `holiday_location` | body | `string` | yes |
| `is_admin` | body | `boolean` | no |
