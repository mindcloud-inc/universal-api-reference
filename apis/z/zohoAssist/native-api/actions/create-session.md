# Create Session with Zoho Assist

Creates a remote support or screen sharing session in Zoho Assist.

## Endpoint

- **Method:** `POST`
- **Path:** `/session`
- **Base URL:** `https://assist.zoho.com/api/v2`
- **Official documentation:** [Create Session](https://www.zoho.com/assist/api/createasession.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_email` | query | `string` | no | Customer email to receive the join invitation. |
| `type` | query | `string` | no | Session type: rs for remote support, dm for screen sharing, cb for cobrowse. |
