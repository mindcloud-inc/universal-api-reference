# List Custom Rewards with Twitch

Retrieves custom reward records from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/channel_points/custom_rewards`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Custom Rewards](https://dev.twitch.tv/docs/api/reference#get-custom-reward)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The ID of the broadcaster whose custom rewards you want to get. |
| `id` | query | `string` | no | A reward ID to filter the custom rewards by. Send multiple values as a array. |
| `only_manageable_rewards` | query | `boolean` | no | Whether to return only rewards that this app may manage. |
