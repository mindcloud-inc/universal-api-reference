# Create Clip with Twitch

Creates a new clip in Twitch.

## Endpoint

- **Method:** `POST`
- **Path:** `/clips`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Create Clip](https://dev.twitch.tv/docs/api/reference#create-clip)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The broadcaster whose live stream to clip. |
| `title` | query | `string` | no | Optional title for the clip. |
| `duration` | query | `number` | no | Clip length in seconds. Possible values range from 5 to 60 with 0.1 precision. Default is 30. |
