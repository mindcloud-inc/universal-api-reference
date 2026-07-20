# Update Allowance Type with Leave Dates

Updates an existing allowance type in Leave Dates.

## Endpoint

- **Method:** `PUT`
- **Path:** `/allowance-types/:id`
- **Base URL:** `https://api.leavedates.com`
- **Official documentation:** [Update Allowance Type](https://api.leavedates.com/documentation#/Company/put_allowance-types__id_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `company_id` | body | `string` | yes |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
