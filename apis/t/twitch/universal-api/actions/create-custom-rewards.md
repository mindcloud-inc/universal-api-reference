# Twitch: Create Custom Rewards

Creates a custom reward in Twitch.

```
POST https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-custom-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-custom-rewards" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcasterId": "string",
  "title": "string",
  "cost": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twitch/latest/actions/create-custom-rewards', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcasterId": "string",
    "title": "string",
    "cost": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcasterId` | string | yes | The ID of the broadcaster to add the custom reward to. |
| `title` | string | yes | The custom reward’s title. |
| `cost` | number | yes | The cost of the reward, in Channel Points. |
| `prompt` | string | no | The prompt shown when a viewer redeems the reward. |
| `isEnabled` | boolean | no | Whether the reward is enabled. |
| `backgroundColor` | string | no | The background color to use for the reward in hex format. |
| `isUserInputRequired` | boolean | no | Whether the viewer must enter input when redeeming the reward. |
| `isMaxPerStreamEnabled` | boolean | no | Whether to limit the maximum number of redemptions allowed per live stream. |
| `maxPerStream` | number | no | The maximum number of redemptions allowed per live stream. |
| `isMaxPerUserPerStreamEnabled` | boolean | no | Whether to limit the maximum number of redemptions allowed per user per live stream. |
| `maxPerUserPerStream` | number | no | The maximum number of redemptions allowed per user per live stream. |
| `isGlobalCooldownEnabled` | boolean | no | Whether to apply a cooldown period between redemptions. |
| `globalCooldownSeconds` | number | no | The cooldown period, in seconds. |
| `shouldRedemptionsSkipRequestQueue` | boolean | no | Whether redemptions should be fulfilled immediately when redeemed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "backgroundColor": "string",
          "broadcasterId": "string",
          "broadcasterLogin": "string",
          "broadcasterName": "Ava Chen",
          "cooldownExpiresAt": "string",
          "cost": 1,
          "defaultImage": {
            "url1x": "https://example.com",
            "url2x": "https://example.com",
            "url4x": "https://example.com"
          },
          "globalCooldownSetting": {
            "globalCooldownSeconds": 1,
            "isEnabled": true
          },
          "id": "string",
          "image": {
            "url1x": "https://example.com",
            "url2x": "https://example.com",
            "url4x": "https://example.com"
          },
          "isEnabled": true,
          "isInStock": true,
          "isPaused": true,
          "isUserInputRequired": true,
          "maxPerStreamSetting": {
            "isEnabled": true,
            "maxPerStream": 1
          },
          "maxPerUserPerStreamSetting": {
            "isEnabled": true,
            "maxPerUserPerStream": 1
          },
          "prompt": "string",
          "redemptionsRedeemedCurrentStream": 1,
          "shouldRedemptionsSkipRequestQueue": true,
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Custom reward rows. |
| `data[].backgroundColor` | string | Reward background color. |
| `data[].broadcasterId` | string | Broadcaster identifier. |
| `data[].broadcasterLogin` | string | Broadcaster login name. |
| `data[].broadcasterName` | string | Broadcaster display name. |
| `data[].cooldownExpiresAt` | string | Cooldown expiry timestamp when the reward is cooling down. |
| `data[].cost` | number | Reward redemption cost in channel points. |
| `data[].defaultImage` | object | Default reward image. |
| `data[].defaultImage.url1x` | string | Default 1x image URL. |
| `data[].defaultImage.url2x` | string | Default 2x image URL. |
| `data[].defaultImage.url4x` | string | Default 4x image URL. |
| `data[].globalCooldownSetting` | object | Global cooldown setting. |
| `data[].globalCooldownSetting.globalCooldownSeconds` | number | Cooldown duration in seconds. |
| `data[].globalCooldownSetting.isEnabled` | boolean | Whether the global cooldown is enabled. |
| `data[].id` | string | Custom reward identifier. |
| `data[].image` | object | Custom reward image when configured. |
| `data[].image.url1x` | string | 1x custom reward image URL. |
| `data[].image.url2x` | string | 2x custom reward image URL. |
| `data[].image.url4x` | string | 4x custom reward image URL. |
| `data[].isEnabled` | boolean | Whether the reward is enabled. |
| `data[].isInStock` | boolean | Whether the reward is in stock. |
| `data[].isPaused` | boolean | Whether the reward is paused. |
| `data[].isUserInputRequired` | boolean | Whether the reward requires viewer input. |
| `data[].maxPerStreamSetting` | object | Maximum redemptions per stream setting. |
| `data[].maxPerStreamSetting.isEnabled` | boolean | Whether the per-stream limit is enabled. |
| `data[].maxPerStreamSetting.maxPerStream` | number | Maximum redemptions allowed per stream. |
| `data[].maxPerUserPerStreamSetting` | object | Per-user redemptions per stream setting. |
| `data[].maxPerUserPerStreamSetting.isEnabled` | boolean | Whether the per-user per-stream limit is enabled. |
| `data[].maxPerUserPerStreamSetting.maxPerUserPerStream` | number | Maximum redemptions per user per stream. |
| `data[].prompt` | string | Prompt shown when user input is required. |
| `data[].redemptionsRedeemedCurrentStream` | number | Redemptions redeemed in the current stream. |
| `data[].shouldRedemptionsSkipRequestQueue` | boolean | Whether redemptions skip the request queue. |
| `data[].title` | string | Reward title. |

## Native endpoint

Through the native Twitch API, this operation is `POST /channel_points/custom_rewards` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-rewards.md) for the provider-specific parameters and requirements.

