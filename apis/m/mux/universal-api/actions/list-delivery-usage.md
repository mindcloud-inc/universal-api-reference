# Mux: List Delivery Usage



```
GET https://connect.mindcloud.co/v1/universal/mux/latest/actions/list-delivery-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mux/latest/actions/list-delivery-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mux/latest/actions/list-delivery-usage?${params}`, {
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
      "data": [
        {}
      ],
      "limit": 1,
      "timeframe": [
        1
      ],
      "totalRowCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `limit` | number |  |
| `timeframe` | array<number> |  |
| `totalRowCount` | number |  |

## Native endpoint

Through the native Mux API, this operation is `GET /video/v1/delivery-usage` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-delivery-usage.md) for the provider-specific parameters and requirements.

