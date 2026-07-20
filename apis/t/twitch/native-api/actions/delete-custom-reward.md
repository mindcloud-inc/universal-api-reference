# Delete Custom Reward with Twitch

Deletes a custom reward from Twitch.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/channel_points/custom_rewards`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Delete Custom Reward](https://dev.twitch.tv/docs/api/reference#delete-custom-reward)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The ID of the broadcaster that created the custom reward. |
| `id` | query | `string` | yes | The ID of the custom reward to delete. |
