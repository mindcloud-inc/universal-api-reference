# Update Meeting with Webex

Updates an existing meeting in Webex.

## Endpoint

- **Method:** `PUT`
- **Path:** `/meetings/:meetingId`
- **Base URL:** `https://webexapis.com/v1`
- **Official documentation:** [Update Meeting](https://developer.webex.com/meeting/docs/api/v1/meetings/update-a-meeting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meetingId` | path | `string` | yes | Meeting identifier. |
| `title` | body | `string` | no | Updated meeting title. |
| `start` | body | `date` | no | Updated meeting start time in ISO-8601 format. |
| `end` | body | `date` | no | Updated meeting end time in ISO-8601 format. |
