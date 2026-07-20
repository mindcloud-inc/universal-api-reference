# Bulk Register Webinar with Zoho Webinar

Creates webinar registrations in Zoho Webinar in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/:organizationId/register/:webinarKey.json`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [Bulk Register Webinar](https://www.zoho.com/webinar/api/webinar-api/bulk-registration.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `webinarKey` | path | `string` | yes |
| `sendMail` | query | `boolean` | no |
| `instanceId` | query | `string` | no |
| `registrant` | body | `list<object>` | yes |
