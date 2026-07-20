# Sunwise: Health

Retrieves service health from Sunwise.

```
GET https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/health
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/health?${params}`, {
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
      "services": {
        "mongo": "string",
        "postgres": "string",
        "redis": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `services.mongo` | string |  |
| `services.postgres` | string |  |
| `services.redis` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Sunwise API, this operation is `GET /health` (base URL `https://production.sunwise.ai/boty/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health.md) for the provider-specific parameters and requirements.

