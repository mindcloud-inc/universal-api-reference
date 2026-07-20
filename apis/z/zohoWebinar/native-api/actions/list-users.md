# List Users with Zoho Webinar

Retrieves users from Zoho Webinar.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/user`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [List Users](https://www.zoho.com/webinar/api/user-api/list-of-users.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `index` | query | `number` | no |
| `count` | query | `number` | no |
