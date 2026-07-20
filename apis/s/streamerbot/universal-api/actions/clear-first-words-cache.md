# Streamer.bot: Clear First Words Cache

Clears the first words cache in Streamer.bot.

```
DELETE https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/clear-first-words-cache
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamer.bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/clear-first-words-cache?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/clear-first-words-cache?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Streamer.bot API returns.

## Native endpoint

Through the native Streamer.bot API, this operation is `GET /ClearFirstWordsCache` (base URL `https://allow-freely-princess-carefully.trycloudflare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-first-words-cache.md) for the provider-specific parameters and requirements.

