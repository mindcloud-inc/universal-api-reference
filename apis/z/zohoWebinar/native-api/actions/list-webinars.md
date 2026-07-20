# List Webinars with Zoho Webinar

Retrieves webinars from Zoho Webinar by list type.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/webinar.json`
- **Base URL:** `https://webinar.zoho.com`
- **Official documentation:** [List Webinars](https://www.zoho.com/webinar/api/webinar-api/list-of-webinars.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `string` | yes |
| `listtype` | query | `string` | yes |
| `index` | query | `number` | yes |
| `count` | query | `number` | yes |
