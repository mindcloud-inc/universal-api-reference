# DateX: Create Sales Orders



```
POST https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/create-sales-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/create-sales-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orders[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/create-sales-orders', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orders[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orders[]` | array<object> | yes | Array of sales order objects to create, matching the documented orders schema. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "carrierService": "string",
      "isBackOrdered": true,
      "lookup": "string",
      "orderClass": "string",
      "orderId": 1,
      "owner": "string",
      "ownerReference": "string",
      "priority": 1,
      "project": "string",
      "requestedDeliveryDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "vendorReference": "string",
      "warehouse": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `carrierService` | string |  |
| `isBackOrdered` | boolean |  |
| `lookup` | string |  |
| `orderClass` | string |  |
| `orderId` | number |  |
| `owner` | string |  |
| `ownerReference` | string |  |
| `priority` | number |  |
| `project` | string |  |
| `requestedDeliveryDate` | date |  |
| `status` | string |  |
| `vendorReference` | string |  |
| `warehouse` | string |  |

## Native endpoint

Through the native DateX API, this operation is `POST sales_orders/create` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-orders.md) for the provider-specific parameters and requirements.

