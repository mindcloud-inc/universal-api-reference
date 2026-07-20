# Megaventory: Cancel Purchase Order

Cancels a purchase order in Megaventory.

```
PUT https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/cancel-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/cancel-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mvPurchaseOrderNoToCancel": "string",
  "mvPurchaseOrderTypeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/cancel-purchase-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mvPurchaseOrderNoToCancel": "string",
    "mvPurchaseOrderTypeId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mvPurchaseOrderNoToCancel` | string | yes | Purchase order number Megaventory should cancel. |
| `mvPurchaseOrderTypeId` | number | yes | Purchase order type ID Megaventory needs for cancellation. |
| `mvInsertUpdateDeleteSourceApplication` | string | no | Source application label Megaventory should store for the change. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ResponseStatus": {},
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ResponseStatus` | object |  |
| `result` | boolean |  |

## Native endpoint

Through the native Megaventory API, this operation is `POST /json/reply/PurchaseOrderCancel` (base URL `https://api.megaventory.com/v2017a`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-purchase-order.md) for the provider-specific parameters and requirements.

