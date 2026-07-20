# Create Leave Request with Zoho People

Creates a leave request in Zoho People.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/leave-tracker/leaves`
- **Base URL:** `https://people.zoho.com`
- **Official documentation:** [Create Leave Request](https://www.zoho.com/people/api/v3/leave-tracker/add-leave.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee_zoho_id` | body | `string` | yes | Zoho employee erecno for the leave request. |
| `leave_type_id` | body | `string` | yes | Zoho leave type ID. |
| `from_date` | body | `string` | yes | Leave start date in the organization date format. |
| `to_date` | body | `string` | yes | Leave end date in the organization date format. |
| `unit` | body | `string` | yes | Leave unit. Zoho documents Days or Hours. |
| `reason` | body | `string` | no | Optional reason for the leave request. |
| `days` | body | `string` | no | Optional JSON object keyed by date with leave_count, session, start_time, and end_time. |
| `approver_id` | body | `string` | no | Optional approver erecno when employees choose an approver. |
