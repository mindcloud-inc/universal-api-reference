# Update Leave Type with Leave Dates

Updates an existing leave type in Leave Dates.

## Endpoint

- **Method:** `PUT`
- **Path:** `/leave-types/:id`
- **Base URL:** `https://api.leavedates.com`
- **Official documentation:** [Update Leave Type](https://api.leavedates.com/documentation#/Company/put_leave-types__id_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `company_id` | body | `string` | yes |
| `allowance_type_id` | body | `string` | yes |
| `name` | body | `string` | yes |
| `display_code` | body | `string` | yes |
| `display_icon` | body | `string` | yes |
| `colour` | body | `string` | yes |
| `approval` | body | `boolean` | yes |
| `is_holiday` | body | `boolean` | yes |
| `only_admin` | body | `boolean` | yes |
| `description` | body | `string` | no |
