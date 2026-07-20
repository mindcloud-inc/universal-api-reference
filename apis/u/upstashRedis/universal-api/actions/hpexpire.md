# Upstash Redis: HPEXPIRE

Executes the HPEXPIRE command in Upstash Redis to set field TTL in milliseconds.

```
POST https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/hpexpire
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upstash Redis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/hpexpire" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/hpexpire', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Upstash Redis API returns.

## Native endpoint

Through the native Upstash Redis API, this operation is `GET /hpexpire` (base URL `https://choice-oriole-98954.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/hpexpire.md) for the provider-specific parameters and requirements.

