# Create Custom Rewards with Twitch

Creates a custom reward in Twitch.

## Endpoint

- **Method:** `POST`
- **Path:** `/channel_points/custom_rewards`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Create Custom Rewards](https://dev.twitch.tv/docs/api/reference#create-custom-rewards)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The ID of the broadcaster to add the custom reward to. |
| `title` | body | `string` | yes | The custom reward’s title. |
| `cost` | body | `number` | yes | The cost of the reward, in Channel Points. |
| `prompt` | body | `string` | no | The prompt shown when a viewer redeems the reward. |
| `is_enabled` | body | `boolean` | no | Whether the reward is enabled. |
| `background_color` | body | `string` | no | The background color to use for the reward in hex format. |
| `is_user_input_required` | body | `boolean` | no | Whether the viewer must enter input when redeeming the reward. |
| `is_max_per_stream_enabled` | body | `boolean` | no | Whether to limit the maximum number of redemptions allowed per live stream. |
| `max_per_stream` | body | `number` | no | The maximum number of redemptions allowed per live stream. |
| `is_max_per_user_per_stream_enabled` | body | `boolean` | no | Whether to limit the maximum number of redemptions allowed per user per live stream. |
| `max_per_user_per_stream` | body | `number` | no | The maximum number of redemptions allowed per user per live stream. |
| `is_global_cooldown_enabled` | body | `boolean` | no | Whether to apply a cooldown period between redemptions. |
| `global_cooldown_seconds` | body | `number` | no | The cooldown period, in seconds. |
| `should_redemptions_skip_request_queue` | body | `boolean` | no | Whether redemptions should be fulfilled immediately when redeemed. |
