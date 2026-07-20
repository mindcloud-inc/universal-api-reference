# Get Stream Key with Twitch

Retrieves a stream key from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/streams/key`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Get Stream Key](https://dev.twitch.tv/docs/api/reference#get-stream-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The ID of the broadcaster that owns the channel. |
