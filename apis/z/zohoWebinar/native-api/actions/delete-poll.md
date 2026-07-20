# Delete Poll with Zoho Webinar

Deletes an existing webinar poll from Zoho Webinar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/meeting/api/v2/:organizationId/poll/:pollId`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [Delete Poll](https://www.zoho.com/webinar/api/polls/delete.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `pollId` | path | `string` | yes |
| `webinarKey` | query | `string` | yes |
| `instanceId` | query | `string` | no |
