# Create Meeting with Zoho Meeting

Creates a new meeting in Zoho Meeting.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/:organizationId/sessions.json`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [Create Meeting](https://www.zoho.com/meeting/api-integration/meeting-api/create-a-meeting.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `session.topic` | body | `string` | yes | Meeting topic. |
| `session.startTime` | body | `string` | yes | Meeting start time in Zoho's expected format. |
| `session.presenter` | body | `string` | yes | Presenter user ID. |
| `session.duration` | body | `number` | no | Meeting duration. |
| `session.timezone` | body | `string` | no | Meeting timezone. |
| `session.agenda` | body | `string` | no | Meeting agenda or description. |
| `session.participants[]` | body | `array<object>` | no | Optional array of participant objects. |
