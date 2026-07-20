# Upstash Redis: Get Key TTL

Retrieves a key TTL from Upstash Redis.

```
GET https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/get-key-ttl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upstash Redis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/get-key-ttl?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/get-key-ttl?${params}`, {
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
| `key` | string | yes | Redis key whose TTL to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | number | TTL in seconds, or Redis sentinel values such as -1 or -2. |

## Native endpoint

Through the native Upstash Redis API, this operation is `GET /ttl/:key` (base URL `https://choice-oriole-98954.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-key-ttl.md) for the provider-specific parameters and requirements.

