# Upstash Redis: BITFIELD_RO

Executes the BITFIELD_RO command in Upstash Redis to read-only bitfield operations.

```
GET https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/bitfield-ro
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upstash Redis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/bitfield-ro?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/bitfield-ro?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Upstash Redis API returns.

## Native endpoint

Through the native Upstash Redis API, this operation is `GET /bitfield_ro` (base URL `https://choice-oriole-98954.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bitfield-ro.md) for the provider-specific parameters and requirements.

