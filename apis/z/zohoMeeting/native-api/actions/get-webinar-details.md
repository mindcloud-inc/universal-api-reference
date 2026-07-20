# Get Webinar Details with Zoho Meeting

Retrieves webinar details from Zoho Meeting.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/webinar/:webinarKey.json`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [Get Webinar Details](https://www.zoho.com/meeting/api-integration/webinar-api/get-webinar-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `webinarKey` | path | `string` | yes | Webinar key returned by List Webinars or Create Webinar. |
