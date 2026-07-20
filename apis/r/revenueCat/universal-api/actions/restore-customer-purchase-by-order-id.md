# RevenueCat: Restore Customer Purchase By Order ID

Restores a Google Play purchase by order ID in RevenueCat.

```
PUT https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/restore-customer-purchase-by-order-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RevenueCat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/restore-customer-purchase-by-order-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/revenueCat/latest/actions/restore-customer-purchase-by-order-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted_at": "string",
      "id": "string",
      "items": [
        {}
      ],
      "metrics": [
        {}
      ],
      "object": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted_at` | string |  |
| `id` | string |  |
| `items` | array<object> |  |
| `metrics` | array<object> |  |
| `object` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native RevenueCat API, this operation is `POST projects/:projectId/customers/:customerId/actions/restore_purchase_by_order_id` (base URL `https://api.revenuecat.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-customer-purchase-by-order-id.md) for the provider-specific parameters and requirements.

