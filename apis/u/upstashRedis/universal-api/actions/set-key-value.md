# Upstash Redis: Set Key Value

Sets a key value in Upstash Redis.

```
POST https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/set-key-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upstash Redis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/set-key-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/set-key-value', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | yes | Redis key to create or overwrite. |
| `value` | string | yes | String value to store. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Set command status from Redis. |

## Native endpoint

Through the native Upstash Redis API, this operation is `GET /set/:key/:value` (base URL `https://choice-oriole-98954.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-key-value.md) for the provider-specific parameters and requirements.

