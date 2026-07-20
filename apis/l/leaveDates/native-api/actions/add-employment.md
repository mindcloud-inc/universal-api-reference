# Add Employment with Leave Dates

Creates a new employment in Leave Dates.

## Endpoint

- **Method:** `POST`
- **Path:** `/employments`
- **Base URL:** `https://api.leavedates.com`
- **Official documentation:** [Add Employment](https://api.leavedates.com/documentation#/Employment/post_employments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | body | `string` | yes | Company ID for the employment |
| `full_name` | body | `string` | yes | Full name of the employee |
| `email` | body | `string` | yes | Employee email address |
| `timezone` | body | `string` | yes | Employment timezone |
| `holiday_location` | body | `string` | yes | Holiday location label |
| `is_admin` | body | `boolean` | no | Whether the employment is an admin user |
