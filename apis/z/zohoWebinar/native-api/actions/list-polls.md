# List Polls with Zoho Webinar

Retrieves webinar polls from Zoho Webinar.

## Endpoint

- **Method:** `GET`
- **Path:** `/meeting/api/v2/:organizationId/poll`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [List Polls](https://www.zoho.com/webinar/api/polls/list.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `index` | query | `number` | no |
| `count` | query | `number` | no |
| `webinarKey` | query | `string` | yes |
| `instanceId` | query | `string` | no |
