# Create Meeting with Dialpad

Creates a new meeting in Dialpad.

## Endpoint

- **Method:** `POST`
- **Path:** `/meetings`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Create Meeting](https://developers.dialpad.com/reference/meetingscreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | body | `number` | yes | The Dialpad user's id. |
| `title` | body | `string` | yes | The meeting's title. |
| `meeting_type` | body | `list<string>` | yes | The meeting's type. Accepted values: `CUSTOM_UNIQUE_MEETING`, `LARGE_MEETING`, `PERSONAL`, `UNIQUE_MEETING`. |
| `start_datetime` | body | `date` | yes | The meeting's start time (UTC seconds-since-epoch timestamp). |
| `end_datetime` | body | `date` | yes | The meeting's end time (UTC seconds-since-epoch timestamp). |
| `duration` | body | `number` | no | Duration of the meeting in seconds. |
| `call_out` | body | `boolean` | no | Whether or not the meeting should call the participants. |
| `recurrence` | body | `string` | no | How often the meeting should be repeated. |
| `participants_info[]` | body | `array<object>` | no | The list of users that participate in the meeting. |
