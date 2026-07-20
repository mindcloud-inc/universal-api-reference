# Revi.io Reviews: Update Order Statuses

Updates order statuses in Revi.io Reviews.

```
PUT https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/update-order-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revi.io Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/update-order-statuses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orders[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/update-order-statuses', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orders[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orders[]` | array<object> | yes | Array of order status objects containing id_order, status, and date_status_upd. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders_count": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orders_count` | number | Number of order statuses processed by Revi. |
| `success` | boolean | Whether the order status payload was accepted. |

## Native endpoint

Through the native Revi.io Reviews API, this operation is `POST /orders_status` (base URL `https://api.revi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order-statuses.md) for the provider-specific parameters and requirements.

