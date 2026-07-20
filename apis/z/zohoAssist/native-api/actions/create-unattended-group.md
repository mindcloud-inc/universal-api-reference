# Create Unattended Group with Zoho Assist

Creates a new unattended computer group in Zoho Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/unattended_computer/group`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [Create Unattended Group](https://www.zoho.com/assist/api/createunattendedgroup.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `department_id` | body | `string` | yes | Department in which the group should be created. |
| `group_name` | body | `string` | yes | Name of the unattended group. |
| `description` | body | `string` | yes | Description for the unattended group. |
| `computer_list[]` | body | `array<string>` | no | Optional list of device IDs to add to the group. |
