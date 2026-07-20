# Upstash Redis: JSON.DEL

Executes the JSON.DEL command in Upstash Redis to delete JSON values.

```
DELETE https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/json-del
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upstash Redis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/json-del?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/json-del?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Upstash Redis API returns.

## Native endpoint

Through the native Upstash Redis API, this operation is `GET /json.del` (base URL `https://choice-oriole-98954.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/json-del.md) for the provider-specific parameters and requirements.

