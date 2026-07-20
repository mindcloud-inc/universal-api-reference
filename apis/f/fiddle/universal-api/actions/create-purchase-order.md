# Fiddle: Create Purchase Order

Creates a new purchase order in Fiddle.

```
POST https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/create-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/create-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "supplierId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fiddle/latest/actions/create-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "supplierId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `supplierId` | string | yes | Supplier ID from Fiddle |

## Response

```json
{
  "success": true,
  "data": [
    {
      "purchaseOrders": [
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
| `purchaseOrders[]` | array<object> |  |
| `purchaseOrders[].createdAt` | date |  |
| `purchaseOrders[].id` | string |  |
| `purchaseOrders[].notes` | string |  |
| `purchaseOrders[].purchaseOrderNumber` | string |  |
| `purchaseOrders[].status` | string |  |
| `purchaseOrders[].supplier` | object |  |
| `purchaseOrders[].supplier.id` | string |  |
| `purchaseOrders[].supplier.name` | string |  |
| `purchaseOrders[].supplierId` | string |  |
| `purchaseOrders[].updatedAt` | date |  |

## Native endpoint

Through the native Fiddle API, this operation is `POST /purchase-orders` (base URL `https://fiddle.io/rest/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order.md) for the provider-specific parameters and requirements.

