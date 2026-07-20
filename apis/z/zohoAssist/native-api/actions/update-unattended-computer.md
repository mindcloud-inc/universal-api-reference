# Update Unattended Computer with Zoho Assist

Updates the display name of an unattended computer in Zoho Assist.

## Endpoint

- **Method:** `PUT`
- **Path:** `/devices/:resourceId`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [Update Unattended Computer](https://www.zoho.com/assist/api/updateunattendedcomputer.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | Device resource ID to update. |
| `departmentId` | path | `string` | yes | — |
| `source` | path | `string` | no | — |
| `display_name` | body | `string` | yes | New display name for the device. |
