# Get Polls Report with Zoho Webinar

Retrieves poll report entries from Zoho Webinar.

## Endpoint

- **Method:** `GET`
- **Path:** `/meeting/api/v2/:organizationId/report/poll`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [Get Polls Report](https://www.zoho.com/webinar/api/reports/polls.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `index` | query | `number` | no |
| `count` | query | `number` | no |
| `webinarKey` | query | `string` | yes |
| `instanceId` | query | `string` | no |
| `category` | query | `number` | no |
