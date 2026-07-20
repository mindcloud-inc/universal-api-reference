# Update Webinar with Zoho Webinar

Updates an existing webinar in Zoho Webinar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/:organizationId/webinar/:webinarKey.json`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [Update Webinar](https://www.zoho.com/webinar/api/webinar-api/edit-webinar.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `webinarKey` | path | `string` | yes |
| `session.topic` | body | `string` | no |
| `session.agenda` | body | `string` | no |
| `session.presenter` | body | `string` | no |
| `session.startTime` | body | `string` | no |
| `session.duration` | body | `number` | no |
| `session.timezone` | body | `string` | no |
