# Get Questions Report with Zoho Webinar

Retrieves question report entries from Zoho Webinar.

## Endpoint

- **Method:** `GET`
- **Path:** `/meeting/api/v2/:organizationId/report/questions`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [Get Questions Report](https://www.zoho.com/webinar/api/reports/question.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `index` | query | `number` | no |
| `count` | query | `number` | no |
| `webinarKey` | query | `string` | yes |
| `instanceId` | query | `string` | no |
