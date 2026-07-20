# Create Leave Type with Leave Dates

Creates a new leave type in Leave Dates.

## Endpoint

- **Method:** `POST`
- **Path:** `/leave-types`
- **Base URL:** `https://api.leavedates.com`
- **Official documentation:** [Create Leave Type](https://api.leavedates.com/documentation#/Company/post_leave-types)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
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
