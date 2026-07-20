# Delete Meeting with Zoho Meeting

Deletes an existing meeting from Zoho Meeting.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/:organizationId/sessions/:meetingKey.json`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [Delete Meeting](https://www.zoho.com/meeting/api-integration/meeting-api/delete-meeting-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `meetingKey` | path | `string` | yes | Meeting key returned by List Meetings or Create Meeting. |
