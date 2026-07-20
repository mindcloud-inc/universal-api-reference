# Get User Details with Zoho Meeting

Retrieves user details from Zoho Meeting.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/user/:userId`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [Get User Details](https://www.zoho.com/meeting/api-integration/user-api/get-user-details.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `userId` | path | `string` | yes | User ID returned by List Users. |
