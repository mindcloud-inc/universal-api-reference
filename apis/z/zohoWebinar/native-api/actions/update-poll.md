# Update Poll with Zoho Webinar

Updates an existing webinar poll in Zoho Webinar.

## Endpoint

- **Method:** `PUT`
- **Path:** `/meeting/api/v2/:organizationId/poll/:pollId`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [Update Poll](https://www.zoho.com/webinar/api/polls/update.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `pollId` | path | `string` | yes |
| `webinarKey` | query | `string` | yes |
| `instanceId` | query | `string` | no |
| `poll` | body | `object` | yes |
