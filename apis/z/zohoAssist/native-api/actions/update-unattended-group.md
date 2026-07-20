# Update Unattended Group with Zoho Assist

Updates an existing unattended computer group in Zoho Assist.

## Endpoint

- **Method:** `PUT`
- **Path:** `/unattended_computer/group`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [Update Unattended Group](https://www.zoho.com/assist/api/updateunattendedgroup.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | ID of the group to update. |
| `department_id` | body | `string` | yes | Department containing the group. |
| `name` | body | `string` | yes | Updated group name. |
| `description` | body | `string` | no | Updated group description. |
| `addedlist[]` | body | `array<string>` | no | Optional device IDs to add to the group. |
| `removedlist[]` | body | `array<string>` | no | Optional device IDs to remove from the group. |
