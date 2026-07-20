# MRPeasy: Update Customer Order

Updates an existing customer order in MRPeasy.

```
PUT https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/update-customer-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MRPeasy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/update-customer-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "custOrdId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/update-customer-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "custOrdId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `custOrdId` | number | yes | MRPeasy customer order ID. |
| `reference` | string | no | Updated customer order reference. |
| `products` | array<object> | no | Updated MRPeasy order line array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MRPeasy API returns.

## Native endpoint

Through the native MRPeasy API, this operation is `PUT /customer-orders/{{custOrdId}}` (base URL `https://api.mrpeasy.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer-order.md) for the provider-specific parameters and requirements.

