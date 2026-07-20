# Create Poll with Zoho Webinar

Creates a new webinar poll in Zoho Webinar.

## Endpoint

- **Method:** `POST`
- **Path:** `/meeting/api/v2/:organizationId/poll`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [Create Poll](https://www.zoho.com/webinar/api/polls/create.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `webinarKey` | query | `string` | yes |
| `instanceId` | query | `string` | no |
| `poll` | body | `object` | yes |
