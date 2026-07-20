# Get Attendees Report with Zoho Webinar

Retrieves attendee report entries from Zoho Webinar.

## Endpoint

- **Method:** `GET`
- **Path:** `/meeting/api/v2/:organizationId/report/attendees`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [Get Attendees Report](https://www.zoho.com/webinar/api/reports/attendees.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `index` | query | `number` | no |
| `count` | query | `number` | no |
| `webinarKey` | query | `string` | yes |
| `instanceId` | query | `string` | no |
