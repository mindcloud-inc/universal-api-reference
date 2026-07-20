# Get Channel Stream Schedule with Twitch

Retrieves channel stream schedules from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/schedule`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Get Channel Stream Schedule](https://dev.twitch.tv/docs/api/reference#get-channel-stream-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The ID of the broadcaster whose streaming schedule you want to get. |
| `id` | query | `string` | no | The ID of the scheduled segment to return. |
| `start_time` | query | `date` | no | A timestamp used to filter for segments that start on or after the specified UTC date and time. |
| `first` | query | `number` | no | The maximum number of segments to return. Maximum: 25. Default: 20. |
