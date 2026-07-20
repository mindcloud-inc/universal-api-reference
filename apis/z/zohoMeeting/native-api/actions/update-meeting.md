# Update Meeting with Zoho Meeting

Updates an existing meeting in Zoho Meeting.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/:organizationId/sessions/:meetingKey.json`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [Update Meeting](https://www.zoho.com/meeting/api-integration/meeting-api/edit-meeting-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `meetingKey` | path | `string` | yes | Meeting key returned by List Meetings or Create Meeting. |
| `session.topic` | body | `string` | no | Meeting topic. |
| `session.startTime` | body | `string` | no | Meeting start time in Zoho's expected format. |
| `session.presenter` | body | `string` | no | Presenter user ID. |
| `session.duration` | body | `number` | no | Meeting duration. |
| `session.timezone` | body | `string` | no | Meeting timezone. |
| `session.agenda` | body | `string` | no | Meeting agenda or description. |
| `session.participants[]` | body | `array<object>` | no | Optional array of participant objects. |
