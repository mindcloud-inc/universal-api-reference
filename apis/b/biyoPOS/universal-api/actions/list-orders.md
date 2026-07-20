# Biyo POS: List Orders

Retrieves order records from Biyo POS.

```
GET https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Biyo POS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biyoPOS/latest/actions/list-orders?${params}`, {
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
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `next` | string |  |
| `previous` | string |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Biyo POS API, this operation is `GET /api/v1/orders/` (base URL `https://mindcloud.biyo.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

