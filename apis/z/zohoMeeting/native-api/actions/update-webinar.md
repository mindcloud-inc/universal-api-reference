# Update Webinar with Zoho Meeting

Updates an existing webinar in Zoho Meeting.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/:organizationId/webinar/:webinarKey.json`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [Update Webinar](https://www.zoho.com/meeting/api-integration/webinar-api/edit-webinar.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `webinarKey` | path | `string` | yes | Webinar key returned by List Webinars or Create Webinar. |
| `session.topic` | body | `string` | no | Webinar topic. |
| `session.startTime` | body | `string` | no | Webinar start time in Zoho's expected format. |
| `session.duration` | body | `number` | no | Webinar duration. |
| `session.timezone` | body | `string` | no | Webinar timezone. |
| `session.agenda` | body | `string` | no | Webinar agenda or description. |
| `session.presenter` | body | `string` | no | Presenter user ID. |
| `session.participants[]` | body | `array<object>` | no | Optional array of participant objects. |
