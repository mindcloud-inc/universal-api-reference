# Svix: Endpoint Stats

Retrieves statistics for a specific Svix endpoint.

```
GET https://connect.mindcloud.co/v1/universal/svix/latest/actions/endpoint-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/endpoint-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/endpoint-stats?${params}`, {
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
      "fail": 1,
      "pending": 1,
      "sending": 1,
      "success": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fail` | number |  |
| `pending` | number |  |
| `sending` | number |  |
| `success` | number |  |

## Native endpoint

Through the native Svix API, this operation is `GET /api/v1/app/{app_id}/endpoint/{endpoint_id}/stats` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/endpoint-stats.md) for the provider-specific parameters and requirements.

