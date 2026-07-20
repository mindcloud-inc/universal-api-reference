# Razorpay: List Orders

Retrieves all order records from Razorpay.

```
GET https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Razorpay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/razorpay/latest/actions/list-orders?${params}`, {
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
      "entity": "string",
      "items": [
        [
          {}
        ]
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
| `entity` | string |  |
| `items[]` | array<object> |  |
| `items[].amount` | number |  |
| `items[].amountDue` | number |  |
| `items[].amountPaid` | object |  |
| `items[].attempts` | number |  |
| `items[].createdAt` | number |  |
| `items[].currency` | string |  |
| `items[].entity` | string |  |
| `items[].id` | string |  |
| `items[].notes` | object |  |
| `items[].notes.source` | string |  |
| `items[].offerId` | object |  |
| `items[].receipt` | string |  |
| `items[].status` | string |  |

## Native endpoint

Through the native Razorpay API, this operation is `GET /v1/orders` (base URL `https://api.razorpay.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

