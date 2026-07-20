# Streamer.bot: Clear Credits

Clears the current credits in Streamer.bot.

```
DELETE https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/clear-credits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamer.bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/clear-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/clear-credits?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Streamer.bot API returns.

## Native endpoint

Through the native Streamer.bot API, this operation is `GET /ClearCredits` (base URL `https://allow-freely-princess-carefully.trycloudflare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-credits.md) for the provider-specific parameters and requirements.

