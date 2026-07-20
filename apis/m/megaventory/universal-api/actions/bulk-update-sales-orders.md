# Megaventory: Bulk Update Sales Orders

Updates sales orders in Megaventory in bulk.

```
PUT https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/bulk-update-sales-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/bulk-update-sales-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "SalesOrders": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/bulk-update-sales-orders', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "SalesOrders": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `SalesOrders` | list<object> | yes | JSON array of sales order objects. |
| `mvInsertUpdateDeleteSourceApplication` | string | no | Source application label Megaventory should store for the change. |
| `AutoInsertBundledProductRows` | boolean | no | Automatically insert bundled product rows when Megaventory supports it. |
| `AutoInsertBatchNumbersToProductRows` | boolean | no | Automatically assign batch numbers to product rows when Megaventory supports it. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ResponseStatus": {},
      "SalesOrdersResponses": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ResponseStatus` | object |  |
| `SalesOrdersResponses` | array<object> |  |

## Native endpoint

Through the native Megaventory API, this operation is `POST /json/reply/SalesOrdersUpdate` (base URL `https://api.megaventory.com/v2017a`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-sales-orders.md) for the provider-specific parameters and requirements.

