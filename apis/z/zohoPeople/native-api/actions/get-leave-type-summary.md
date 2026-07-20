# Get Leave Type Summary with Zoho People

Retrieves leave type summary from Zoho People.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/leave-tracker/reports/leave-type-summary/:leaveTypeId`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Get Leave Type Summary](https://www.zoho.com/people/api/v3/leave/reports/leave-type-summary.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leaveTypeId` | path | `string` | yes | Leave type ID for the summary report. |
| `from_date` | query | `string` | yes | Start date for the report, in the organization date format. |
| `to_date` | query | `string` | yes | End date for the report, in the organization date format. |
| `offset` | query | `number` | no | Start index for the report rows to fetch. |
| `limit` | query | `number` | no | Optional maximum number of rows to fetch. |
| `employee_zoho_ids` | query | `string` | no | Optional JSON array of employee erecnos to include. |
| `employee_department_ids` | query | `string` | no | Optional JSON array of department IDs to include. |
| `employee_designation_ids` | query | `string` | no | Optional JSON array of designation IDs to include. |
| `employee_location_ids` | query | `string` | no | Optional JSON array of location IDs to include. |
| `employee_role_ids` | query | `string` | no | Optional JSON array of role IDs to include. |
| `employee_status` | query | `string` | no | Optional JSON array of employee status values such as ACTIVE_USERS or EX_EMPLOYEES. |
