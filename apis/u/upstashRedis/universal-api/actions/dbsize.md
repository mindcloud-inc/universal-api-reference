# Upstash Redis: DBSIZE

Executes the DBSIZE command in Upstash Redis to get number of keys in database.

```
GET https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/dbsize
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upstash Redis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/dbsize?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upstashRedis/latest/actions/dbsize?${params}`, {
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
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | number | Numeric result returned by Redis. |

## Native endpoint

Through the native Upstash Redis API, this operation is `GET /dbsize` (base URL `https://choice-oriole-98954.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/dbsize.md) for the provider-specific parameters and requirements.

