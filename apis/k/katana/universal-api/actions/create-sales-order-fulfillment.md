# Katana: Create Sales Order Fulfillment

Creates a sales order fulfillment in Katana.

```
POST https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-sales-order-fulfillment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-sales-order-fulfillment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "salesOrderId": 1,
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-sales-order-fulfillment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "salesOrderId": 1,
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `salesOrderId` | number | yes |  |
| `pickedDate` | string | no |  |
| `status` | string | yes |  |
| `conversionRate` | number | no |  |
| `conversionDate` | string | no |  |
| `trackingNumber` | string | no |  |
| `trackingUrl` | string | no |  |
| `trackingCarrier` | string | no |  |
| `trackingMethod` | string | no |  |
| `salesOrderFulfillmentRows[]` | array<object> | no |  |
| `salesOrderFulfillmentRows[].salesOrderRowId` | number | no |  |
| `salesOrderFulfillmentRows[].quantity` | number | no |  |
| `salesOrderFulfillmentRows[].batchTransactions[]` | array<object> | no |  |
| `salesOrderFulfillmentRows[].batchTransactions[].batchId` | number | no |  |
| `salesOrderFulfillmentRows[].batchTransactions[].quantity` | number | no |  |
| `salesOrderFulfillmentRows[].serialNumbers[]` | array<number> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversionDate": "string",
      "conversionRate": 1,
      "id": 1,
      "pickedDate": "string",
      "salesOrderFulfillmentRows": [
        {
          "batchTransactions": [
            {
              "batchId": 1,
              "quantity": 1
            }
          ],
          "id": 1,
          "quantity": 1,
          "salesOrderRowId": 1,
          "serialNumbers": [
            1
          ]
        }
      ],
      "salesOrderId": 1,
      "status": "string",
      "trackingCarrier": "string",
      "trackingMethod": "string",
      "trackingNumber": "string",
      "trackingUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversionDate` | string |  |
| `conversionRate` | number |  |
| `id` | number |  |
| `pickedDate` | string |  |
| `salesOrderFulfillmentRows` | array<object> |  |
| `salesOrderFulfillmentRows[].batchTransactions` | array<object> |  |
| `salesOrderFulfillmentRows[].batchTransactions[].batchId` | number |  |
| `salesOrderFulfillmentRows[].batchTransactions[].quantity` | number |  |
| `salesOrderFulfillmentRows[].id` | number |  |
| `salesOrderFulfillmentRows[].quantity` | number |  |
| `salesOrderFulfillmentRows[].salesOrderRowId` | number |  |
| `salesOrderFulfillmentRows[].serialNumbers` | array<number> |  |
| `salesOrderId` | number |  |
| `status` | string |  |
| `trackingCarrier` | string |  |
| `trackingMethod` | string |  |
| `trackingNumber` | string |  |
| `trackingUrl` | string |  |

## Native endpoint

Through the native Katana API, this operation is `POST /sales_order_fulfillments` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-order-fulfillment.md) for the provider-specific parameters and requirements.

