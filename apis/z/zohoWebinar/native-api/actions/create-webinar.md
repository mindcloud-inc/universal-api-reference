# Create Webinar with Zoho Webinar

Creates a new webinar in Zoho Webinar.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/:organizationId/webinar.json`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [Create Webinar](https://www.zoho.com/webinar/api/webinar-api/create-a-webinar.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `session.topic` | body | `string` | yes |
| `session.agenda` | body | `string` | no |
| `session.presenter` | body | `string` | no |
| `session.startTime` | body | `string` | yes |
| `session.duration` | body | `number` | no |
| `session.timezone` | body | `string` | no |
