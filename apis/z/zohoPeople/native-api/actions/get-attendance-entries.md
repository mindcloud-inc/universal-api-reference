# Get Attendance Entries with Zoho People

Retrieves attendance entries from Zoho People.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/attendance/entries`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Get Attendance Entries](https://www.zoho.com/people/api/v3/attendance/entries.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee_zoho_id` | query | `number` | no | Optional Zoho employee ID. |
| `employee_email_id` | query | `string` | no | Optional employee email identifier. |
| `employee_biometric_mapper_id` | query | `string` | no | Optional employee biometric mapper identifier. |
| `employee_id` | query | `string` | no | Optional employee ID. |
| `from_date` | query | `string` | no | Optional start date in the organization date format. |
| `to_date` | query | `string` | no | Optional end date in the organization date format. |
| `last_modified_within` | query | `number` | no | Fetch entries created or updated within the last N minutes. |
| `group_entries_by_date` | query | `boolean` | no | Group attendance entries by date. |
| `group_entries_by_employee` | query | `boolean` | no | Group attendance entries by employee. |
| `offset` | query | `number` | no | Start index for the attendance rows to fetch. |
