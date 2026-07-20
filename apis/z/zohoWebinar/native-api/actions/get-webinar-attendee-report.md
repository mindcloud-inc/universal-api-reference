# Get Webinar Attendee Report with Zoho Webinar

Retrieves webinar attendee report entries from Zoho Webinar.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/attendee/:webinarKey.json`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [Get Webinar Attendee Report](https://www.zoho.com/webinar/api/webinar-api/attendee-report.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `webinarKey` | path | `string` | yes |
| `index` | query | `number` | yes |
| `count` | query | `number` | yes |
