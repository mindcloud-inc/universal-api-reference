# Create Webinar with Zoho Meeting

Creates a new webinar in Zoho Meeting.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/:organizationId/webinar.json`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [Create Webinar](https://www.zoho.com/meeting/api-integration/webinar-api/create-a-webinar.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `session.topic` | body | `string` | yes | Webinar topic. |
| `session.startTime` | body | `string` | yes | Webinar start time in Zoho's expected format. |
| `session.duration` | body | `number` | no | Webinar duration. |
| `session.timezone` | body | `string` | no | Webinar timezone. |
| `session.agenda` | body | `string` | no | Webinar agenda or description. |
| `session.presenter` | body | `string` | no | Presenter user ID. |
| `session.participants[]` | body | `array<object>` | no | Optional array of participant objects. |
