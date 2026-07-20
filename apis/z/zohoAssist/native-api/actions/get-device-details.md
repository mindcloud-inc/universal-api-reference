# Get Device Details with Zoho Assist

Gets details for an unattended device in Zoho Assist.

## Endpoint

- **Method:** `GET`
- **Path:** `/devices/:resourceId`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [Get Device Details](https://www.zoho.com/assist/api/getDeviceDetails.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | Device resource ID to fetch. |
| `departmentId` | path | `string` | yes | Department containing the target device. |
| `source` | path | `string` | no | Optional request source tag sent as a Zoho Assist header. |
