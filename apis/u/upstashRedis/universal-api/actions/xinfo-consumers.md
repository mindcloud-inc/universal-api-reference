# Upstash Redis: XINFO CONSUMERS

Executes the XINFO CONSUMERS command in Upstash Redis to list group consumers.

```
GET https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/xinfo-consumers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upstash Redis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/xinfo-consumers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/xinfo-consumers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Upstash Redis API returns.

## Native endpoint

Through the native Upstash Redis API, this operation is `GET /xinfo/consumers` (base URL `https://choice-oriole-98954.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/xinfo-consumers.md) for the provider-specific parameters and requirements.

