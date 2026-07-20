# Create Webinar Registrations with Zoho Meeting

Creates webinar registrations in bulk in Zoho Meeting.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/:organizationId/register/:webinarKey.json`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [Create Webinar Registrations](https://www.zoho.com/meeting/api-integration/webinar-api/bulk-registration-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `webinarKey` | path | `string` | yes | Webinar key returned by List Webinars or Create Webinar. |
| `sendMail` | query | `boolean` | no | Whether to send webinar registration emails. |
| `instanceId` | query | `string` | no | Event instance ID when required by Zoho. |
| `registrant[]` | body | `array<object>` | yes | Array of registrant objects with email, firstName, and lastName. |
