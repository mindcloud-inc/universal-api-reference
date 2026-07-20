# Streamer.bot: Test Credits

Tests the current credits data in Streamer.bot.

```
GET https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/test-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamer.bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/test-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/test-credits?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "custom": {},
      "events": {},
      "hypeTrainConductor": [
        {}
      ],
      "hypeTrainContributors": [
        {}
      ],
      "topBits": {},
      "topChannelRewards": [
        {}
      ],
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom` | object | Custom test credit values. |
| `events` | object | Grouped test credit event collections. |
| `hypeTrainConductor` | array<object> | Top hype train conductor rows. |
| `hypeTrainContributors` | array<object> | Hype train contributor rows. |
| `topBits` | object | Top bits leaderboards. |
| `topChannelRewards` | array<object> | Top channel reward rows. |
| `user` | object | Grouped user credit collections. |

## Native endpoint

Through the native Streamer.bot API, this operation is `GET /TestCredits` (base URL `https://allow-freely-princess-carefully.trycloudflare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-credits.md) for the provider-specific parameters and requirements.

