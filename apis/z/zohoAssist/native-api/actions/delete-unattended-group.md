# Delete Unattended Group with Zoho Assist

Deletes existing unattended computer groups from Zoho Assist.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/unattended_computer/group`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [Delete Unattended Group](https://www.zoho.com/assist/api/deleteunattendedgroup.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_list[]` | body | `array<string>` | yes | List of unattended group IDs to delete. |
| `department_id` | body | `string` | yes | Department in which the listed groups should be deleted. |
