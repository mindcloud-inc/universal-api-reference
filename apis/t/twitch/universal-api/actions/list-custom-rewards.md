# Twitch: List Custom Rewards

Retrieves custom reward records from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-custom-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-custom-rewards?connectionId=$CONNECTION_ID&broadcasterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcasterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-custom-rewards?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcasterId` | string | yes | The ID of the broadcaster whose custom rewards you want to get. |
| `id` | string | no | A reward ID to filter the custom rewards by. Accepts multiple values as an array. |
| `onlyManageableRewards` | boolean | no | Whether to return only rewards that this app may manage. |

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

Through the native Twitch API, this operation is `GET /channel_points/custom_rewards` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-rewards.md) for the provider-specific parameters and requirements.

