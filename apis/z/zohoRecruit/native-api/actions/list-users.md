# List Users with Zoho Recruit

Retrieves all users from Zoho Recruit.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [List Users](https://www.zoho.com/recruit/developer-guide/apiv2/get-users.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Optional user type filter such as AllUsers, ActiveUsers, AdminUsers, or CurrentUser. |
