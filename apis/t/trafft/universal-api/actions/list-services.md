# Trafft: List Services

Retrieves services from Trafft.

```
GET https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trafft `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-services?${params}`, {
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
      "data": {
        "buffer_time_after": 1,
        "buffer_time_before": 1,
        "duration": 1,
        "id": 1,
        "name": "Ava Chen",
        "price": 1
      },
      "pagination": {
        "limit": 1,
        "page": 1,
        "pages": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.buffer_time_after` | number |  |
| `data.buffer_time_before` | number |  |
| `data.duration` | number |  |
| `data.id` | number |  |
| `data.name` | string |  |
| `data.price` | number |  |
| `pagination` | object |  |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |
| `pagination.total` | number |  |

## Native endpoint

Through the native Trafft API, this operation is `GET /services` (base URL `https://mindcloud.admin.trafft.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

