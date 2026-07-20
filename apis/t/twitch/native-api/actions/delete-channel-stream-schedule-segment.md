# Delete Channel Stream Schedule Segment with Twitch

Deletes a stream schedule segment from Twitch.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/schedule/segment`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Delete Channel Stream Schedule Segment](https://dev.twitch.tv/docs/api/reference#delete-channel-stream-schedule-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The ID of the broadcaster that owns the streaming schedule. |
| `id` | query | `string` | yes | The ID of the broadcast segment to remove. |
