# Quantum Digital: List Orders



```
GET https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantum Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/list-orders?${params}`, {
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
      "orders": [
        {}
      ],
      "paging": {},
      "rowEnd": 1,
      "rowStart": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orders` | array<object> | Order records returned by Quantum Digital. |
| `paging` | object | Paging metadata returned by the provider. |
| `rowEnd` | number | Zero-based row index where the page ends. |
| `rowStart` | number | Zero-based row index where the page starts. |
| `totalCount` | number | Total number of orders across the result set. |

## Native endpoint

Through the native Quantum Digital API, this operation is `GET /v1/orders` (base URL `https://api.quantumdigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

