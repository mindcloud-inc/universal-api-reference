# Ordoro: List Manufacturing Orders

Retrieves manufacturing orders from Ordoro.

```
GET https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/list-manufacturing-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ordoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/list-manufacturing-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/list-manufacturing-orders?${params}`, {
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
      "count": 1,
      "limit": 1,
      "manufacturingOrder": [
        {}
      ],
      "offset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `limit` | number |  |
| `manufacturingOrder` | array<object> |  |
| `offset` | number |  |

## Native endpoint

Through the native Ordoro API, this operation is `GET /v3/manufacturing_order` (base URL `https://api.ordoro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-manufacturing-orders.md) for the provider-specific parameters and requirements.

