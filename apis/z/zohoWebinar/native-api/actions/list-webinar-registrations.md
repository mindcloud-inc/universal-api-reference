# List Webinar Registrations with Zoho Webinar

Retrieves webinar registrations from Zoho Webinar.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/registration/:webinarKey`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [List Webinar Registrations](https://www.zoho.com/webinar/api/webinar-api/registration.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `webinarKey` | path | `string` | yes |
| `index` | query | `number` | no |
| `count` | query | `number` | no |
| `status` | query | `number` | yes |
| `sysId` | query | `string` | no |
