# Get Meeting Details with Zoho Meeting

Retrieves meeting details from Zoho Meeting.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/:organizationId/sessions/:meetingKey.json`
- **Base URL:** `https://meeting.zoho.com`
- **Official documentation:** [Get Meeting Details](https://www.zoho.com/meeting/api-integration/meeting-api/get-meeting-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Organization ID (zsoid) from Get Current User Details. |
| `meetingKey` | path | `string` | yes | Meeting key returned by List Meetings or Create Meeting. |
