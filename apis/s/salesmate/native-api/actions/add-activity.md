# Add Activity with Salesmate

## Endpoint

- **Method:** `POST`
- **Path:** `/activity/v4`
- **Base URL:** `https://apis.salesmate.io`
- **Official documentation:** [Add Activity](https://apidocs.salesmate.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Activity title. |
| `owner` | body | `number` | yes | Salesmate user ID that owns the activity. |
| `type` | body | `string` | yes | Activity type such as Call or Meeting. |
| `dueDate` | body | `date` | no | Activity due date/time. |
| `description` | body | `string` | no | Internal activity description. |
| `duration` | body | `number` | no | Activity duration in minutes. |
| `primaryContact` | body | `number` | no | Primary contact linked to the activity. |
| `tags` | body | `string` | no | Comma-separated tag list. |
| `isCalendarInvite` | body | `boolean` | no | Whether Salesmate should send a calendar invite. |
| `isCompleted` | body | `boolean` | no | Whether the activity is already completed. |
| `followers[]` | body | `array<object>` | no | Follower objects such as { userId } or { contactId }. |
