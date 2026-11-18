# Brightpearl: Update Order



```
PUT https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": 1,
  "operations[]": [
    {}
  ],
  "operations[].op": "remove",
  "operations[].path": "/delivery/deliveryDate"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": 1,
    "operations[]": [{}],
    "operations[].op": "remove",
    "operations[].path": "/delivery/deliveryDate"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderId` | number | yes |  |
| `operations[]` | array<object> | yes |  |
| `operations[].op` | list<string> | yes | One of: `remove`, `replace`. |
| `operations[].path` | list<string> | yes | One of: `/delivery/deliveryDate`, `/delivery/shippingMethodId`, `/parties/billing/contactId`, `/parties/customer/contactId`, `/reference`, `/warehouseId`. |
| `operations[].value` | string | no | Required for replace; omit for remove. IDs are accepted as strings in the documented PATCH examples. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Brightpearl API returns.

## Native endpoint

Through the native Brightpearl API, this operation is `PATCH /order-service/order/:orderId` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

