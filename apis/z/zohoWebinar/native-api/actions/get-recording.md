# Get Recording with Zoho Webinar

Retrieves recording details from Zoho Webinar.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/recordings/:webinarKey.json`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [Get Recording](https://www.zoho.com/webinar/api/recording-api/get-specific-recording.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `webinarKey` | path | `string` | yes |
