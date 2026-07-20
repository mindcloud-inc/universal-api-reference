# Faraday: Get Usage Stats

Retrieves account usage stats from Faraday.

```
GET https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-usage-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faraday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-usage-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faraday/latest/actions/get-usage-stats?${params}`, {
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
      "description": "string",
      "limit": 1,
      "name": "Ava Chen",
      "usage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Usage metric description. |
| `limit` | number | Plan limit. |
| `name` | string | Usage metric name. |
| `usage` | number | Current usage value. |

## Native endpoint

Through the native Faraday API, this operation is `GET /usages` (base URL `https://api.faraday.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage-stats.md) for the provider-specific parameters and requirements.

