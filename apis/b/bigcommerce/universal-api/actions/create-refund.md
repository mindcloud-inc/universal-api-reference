# BigCommerce: Create Refund



```
POST https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-refund" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[]": [
    {}
  ],
  "items[].item_type": "0",
  "order_id": "string",
  "items[].amount": 1,
  "items[].item_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/create-refund', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[]": [{}],
    "items[].item_type": "0",
    "order_id": "string",
    "items[].amount": 1,
    "items[].item_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[]` | array<object> | yes |  |
| `items[].item_type` | string<object> | yes | Default: `0`. |
| `payments[].provider_id` | string<object> | no |  |
| `items[].reason` | string<object> | no | Default: `Customer Requested Refund`. |
| `order_id` | string | yes |  |
| `payments[].amount` | number<object> | no |  |
| `items[].amount` | number<object> | yes |  |
| `payments[]` | array<object> | no |  |
| `payments[].offline` | boolean<object> | no | Whether the payment was marked as offline or performed through an online payment service. Example: true |
| `items[].item_id` | number<object> | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `POST /v3/orders/:order_id/payment_actions/refunds` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-refund.md) for the provider-specific parameters and requirements.

