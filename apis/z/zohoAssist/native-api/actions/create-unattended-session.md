# Create Unattended Session with Zoho Assist

Creates an unattended remote session for a Zoho Assist device.

## Endpoint

- **Method:** `POST`
- **Path:** `/unattended/:resourceId/connect`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [Create Unattended Session](https://www.zoho.com/assist/api/unattendedsession.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceId` | path | `string` | yes | Device resource ID to connect to. |
| `department_id` | query | `string` | yes | Department containing the target device. |
| `osName` | query | `string` | no | Target operating system for Windows or Linux devices. |
| `user_id` | query | `string` | no | Logged-on user ID when required by the device OS. |
