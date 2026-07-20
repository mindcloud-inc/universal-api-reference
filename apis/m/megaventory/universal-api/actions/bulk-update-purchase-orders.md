# Megaventory: Bulk Update Purchase Orders

Updates purchase orders in Megaventory in bulk.

```
PUT https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/bulk-update-purchase-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/bulk-update-purchase-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "PurchaseOrders": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/bulk-update-purchase-orders', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "PurchaseOrders": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `PurchaseOrders` | list<object> | yes | JSON array of purchase order objects. |
| `mvInsertUpdateDeleteSourceApplication` | string | no | Source application label Megaventory should store for the change. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "PurchaseOrdersResponses": [
        {}
      ],
      "ResponseStatus": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `PurchaseOrdersResponses` | array<object> |  |
| `ResponseStatus` | object |  |

## Native endpoint

Through the native Megaventory API, this operation is `POST /json/reply/PurchaseOrdersUpdate` (base URL `https://api.megaventory.com/v2017a`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-purchase-orders.md) for the provider-specific parameters and requirements.

