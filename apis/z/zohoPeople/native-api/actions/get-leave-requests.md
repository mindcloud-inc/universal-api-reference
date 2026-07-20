# Get Leave Requests with Zoho People

Retrieves leave requests from Zoho People.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/leave-tracker/leaves`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Get Leave Requests](https://www.zoho.com/people/api/v3/leave-tracker/get-leave.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_date` | query | `string` | yes | Start date for the leave search, in the organization date format. |
| `to_date` | query | `string` | yes | End date for the leave search, in the organization date format. |
| `data_select` | query | `string` | no | Choose which employee scope to fetch, such as MINE, SUBORDINATES, or ALL. |
| `approval_status` | query | `string` | no | Filter by approval status. Zoho defaults this to ALL. |
| `offset` | query | `number` | no | Start index for the leave records to fetch. |
| `limit` | query | `number` | no | Optional maximum number of leave records to fetch. |
| `sort` | query | `string` | no | Sort expression such as leave_type, -leave_type, employee, or -from_date. |
| `employee_zoho_ids` | query | `string` | no | Optional JSON array of employee erecnos to filter by. |
| `employee_department_ids` | query | `string` | no | Optional JSON array of department IDs to filter by. |
| `employee_location_ids` | query | `string` | no | Optional JSON array of location IDs to filter by. |
| `employee_status` | query | `string` | no | Optional JSON array of status values such as ACTIVE_USERS or EX_EMPLOYEES. |
| `leave_type_ids` | query | `string` | no | Optional JSON array of leave type IDs to filter by. |
| `type_of_leave` | query | `string` | no | Optional JSON array of leave categories such as PAID or UNPAID. |
