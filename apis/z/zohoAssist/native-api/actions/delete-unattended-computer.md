# Delete Unattended Computer with Zoho Assist

Deletes an unattended computer from Zoho Assist.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/devices/:resourceId`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [Delete Unattended Computer](https://www.zoho.com/assist/api/deleteunattendedcomputer.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | Device resource ID to delete. |
| `departmentId` | path | `string` | yes | Department containing the target device. |
| `source` | path | `string` | no | Optional request source tag sent as a Zoho Assist header. |
