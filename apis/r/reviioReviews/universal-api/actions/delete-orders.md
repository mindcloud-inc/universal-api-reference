# Revi.io Reviews: Delete Orders

Deletes orders from Revi.io Reviews.

```
DELETE https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/delete-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revi.io Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/delete-orders?connectionId=$CONNECTION_ID&orders%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orders[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/delete-orders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orders[]` | array<object> | yes | Array of orders to delete using delete=1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order_count": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order_count` | number | Number of deleted orders processed by Revi. |
| `success` | boolean | Whether the delete payload was accepted. |

## Native endpoint

Through the native Revi.io Reviews API, this operation is `POST /orders` (base URL `https://api.revi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-orders.md) for the provider-specific parameters and requirements.

