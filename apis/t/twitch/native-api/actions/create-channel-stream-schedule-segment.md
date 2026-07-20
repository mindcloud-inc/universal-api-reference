# Create Channel Stream Schedule Segment with Twitch

Creates a stream schedule segment in Twitch.

## Endpoint

- **Method:** `POST`
- **Path:** `/schedule/segment`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Create Channel Stream Schedule Segment](https://dev.twitch.tv/docs/api/reference#create-channel-stream-schedule-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The broadcaster whose schedule to update. This ID must match the user ID in the access token. |
| `start_time` | body | `string` | yes | RFC3339 timestamp for the scheduled segment, for example 2026-03-13T18:30:00Z. |
| `timezone` | body | `list` | yes | IANA time zone where the broadcast takes place. |
| `duration` | body | `number` | yes | Scheduled length in minutes. Twitch requires a value from 30 through 1380. |
| `is_recurring` | body | `boolean` | no | Whether the broadcast recurs weekly. |
| `category_id` | body | `string` | no | Category/game ID that best represents the broadcast content. |
| `title` | body | `string` | no | Broadcast title. Maximum 140 characters. Maximum length: 140. |
