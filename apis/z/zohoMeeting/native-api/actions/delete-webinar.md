# Delete Webinar with Zoho Meeting

Deletes an existing webinar from Zoho Meeting.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/:organizationId/webinar/:webinarKey.json`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [Delete Webinar](https://www.zoho.com/meeting/api-integration/webinar-api/delete-webinar-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `webinarKey` | path | `string` | yes | Webinar key returned by List Webinars or Create Webinar. |
