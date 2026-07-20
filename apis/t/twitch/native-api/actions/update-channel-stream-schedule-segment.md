# Update Channel Stream Schedule Segment with Twitch

Updates a stream schedule segment in Twitch.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/schedule/segment`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Update Channel Stream Schedule Segment](https://dev.twitch.tv/docs/api/reference#update-channel-stream-schedule-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The ID of the broadcaster who owns the broadcast segment. |
| `id` | query | `string` | yes | The ID of the broadcast segment to update. |
| `start_time` | body | `string` | no | The date and time that the broadcast segment starts in RFC3339 format. |
| `duration` | body | `number` | no | The length of time, in minutes, that the broadcast is scheduled to run. |
| `category_id` | body | `string` | no | The ID of the category that best represents the broadcast’s content. |
| `title` | body | `string` | no | The broadcast segment title. |
| `is_canceled` | body | `boolean` | no | Whether to cancel the scheduled segment. |
| `timezone` | body | `list` | no | The IANA time zone where the broadcast takes place. |
