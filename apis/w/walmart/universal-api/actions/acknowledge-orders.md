# Walmart: Acknowledge Orders

Acknowledge an entire order, including all of its order lines.

```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/acknowledge-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/acknowledge-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaseOrderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/acknowledge-orders', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "purchaseOrderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaseOrderId` | string | yes | Unique Walmart purchaseOrderId that identifies the purchase order. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isDynamicSandbox` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerEmailId": "ava@example.com",
      "customerOrderId": "string",
      "orderDate": 1,
      "orderLines": {
        "orderLine": [
          {
            "charges": {
              "charge": [
                {
                  "chargeAmount": {
                    "amount": 1,
                    "currency": "string"
                  },
                  "chargeName": "Ava Chen",
                  "chargeType": "string",
                  "tax": {
                    "taxAmount": {
                      "amount": 1,
                      "currency": "string"
                    },
                    "taxName": "Ava Chen"
                  }
                }
              ]
            },
            "fulfillment": {
              "fulfillmentOption": "string",
              "pickUpDateTime": 1,
              "shipMethod": "string",
              "shippingConfigSource": "string",
              "shippingProgramType": "string",
              "shippingSLA": "string"
            },
            "item": {
              "productName": "Ava Chen",
              "sku": "string"
            },
            "lineNumber": "string",
            "orderLineQuantity": {
              "amount": "string",
              "unitOfMeasurement": "string"
            },
            "orderLineStatuses": {
              "orderLineStatus": [
                {
                  "cancellationReason": "string",
                  "status": "string",
                  "statusQuantity": {
                    "amount": "string",
                    "unitOfMeasurement": "string"
                  }
                }
              ]
            },
            "statusDate": 1
          }
        ]
      },
      "purchaseOrderId": "string",
      "shipNode": {
        "type": "string"
      },
      "shippingInfo": {
        "estimatedDeliveryDate": 1,
        "estimatedShipDate": 1,
        "methodCode": "string",
        "phone": "string",
        "postalAddress": {
          "address1": "string",
          "addressType": "string",
          "city": "string",
          "country": "string",
          "name": "Ava Chen",
          "postalCode": "string",
          "state": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerEmailId` | string |  |
| `customerOrderId` | string |  |
| `orderDate` | number |  |
| `orderLines.orderLine[].charges.charge[].chargeAmount.amount` | number |  |
| `orderLines.orderLine[].charges.charge[].chargeAmount.currency` | string |  |
| `orderLines.orderLine[].charges.charge[].chargeName` | string |  |
| `orderLines.orderLine[].charges.charge[].chargeType` | string |  |
| `orderLines.orderLine[].charges.charge[].tax.taxAmount.amount` | number |  |
| `orderLines.orderLine[].charges.charge[].tax.taxAmount.currency` | string |  |
| `orderLines.orderLine[].charges.charge[].tax.taxName` | string |  |
| `orderLines.orderLine[].fulfillment.fulfillmentOption` | string |  |
| `orderLines.orderLine[].fulfillment.pickUpDateTime` | number |  |
| `orderLines.orderLine[].fulfillment.shipMethod` | string |  |
| `orderLines.orderLine[].fulfillment.shippingConfigSource` | string |  |
| `orderLines.orderLine[].fulfillment.shippingProgramType` | string |  |
| `orderLines.orderLine[].fulfillment.shippingSLA` | string |  |
| `orderLines.orderLine[].item.productName` | string |  |
| `orderLines.orderLine[].item.sku` | string |  |
| `orderLines.orderLine[].lineNumber` | string |  |
| `orderLines.orderLine[].orderLineQuantity.amount` | string |  |
| `orderLines.orderLine[].orderLineQuantity.unitOfMeasurement` | string |  |
| `orderLines.orderLine[].orderLineStatuses.orderLineStatus[].cancellationReason` | string |  |
| `orderLines.orderLine[].orderLineStatuses.orderLineStatus[].status` | string |  |
| `orderLines.orderLine[].orderLineStatuses.orderLineStatus[].statusQuantity.amount` | string |  |
| `orderLines.orderLine[].orderLineStatuses.orderLineStatus[].statusQuantity.unitOfMeasurement` | string |  |
| `orderLines.orderLine[].statusDate` | number |  |
| `purchaseOrderId` | string |  |
| `shipNode.type` | string |  |
| `shippingInfo.estimatedDeliveryDate` | number |  |
| `shippingInfo.estimatedShipDate` | number |  |
| `shippingInfo.methodCode` | string |  |
| `shippingInfo.phone` | string |  |
| `shippingInfo.postalAddress.address1` | string |  |
| `shippingInfo.postalAddress.addressType` | string |  |
| `shippingInfo.postalAddress.city` | string |  |
| `shippingInfo.postalAddress.country` | string |  |
| `shippingInfo.postalAddress.name` | string |  |
| `shippingInfo.postalAddress.postalCode` | string |  |
| `shippingInfo.postalAddress.state` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/orders/:purchaseOrderId/acknowledge` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/acknowledge-orders.md) for the provider-specific parameters and requirements.

