# Framework360: Create Order



```
POST https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userEmail": "ava@example.com",
  "cart[]": [
    {}
  ],
  "billingData": {},
  "shippingData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userEmail": "ava@example.com",
    "cart[]": [{}],
    "billingData": {},
    "shippingData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userEmail` | string | yes | Email of the user placing the order. |
| `cart[]` | array<object> | yes | Items included in the order cart. |
| `billingData` | object | yes | Billing data for the order. |
| `shippingData` | object | yes | Shipping data for the order. |
| `shippingId` | number | no | Shipping method ID. |
| `orderStatus` | number | no | Initial order status. |
| `paymentId` | string | no | Payment method ID. |
| `labels[]` | array<string> | no | Labels to assign to the order. |
| `note` | string | no | Additional order notes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Framework360 API returns.

## Native endpoint

Through the native Framework360 API, this operation is `POST orders/create` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/orders-create.md) for the provider-specific parameters and requirements.

