# Create Allowance Type with Leave Dates

Creates a new allowance type in Leave Dates.

## Endpoint

- **Method:** `POST`
- **Path:** `/allowance-types`
- **Base URL:** `https://api.leavedates.com`
- **Official documentation:** [Create Allowance Type](https://api.leavedates.com/documentation#/Company/post_allowance-types)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | body | `string` | yes |
| `name` | body | `string` | yes |
| `description` | body | `string` | no |
