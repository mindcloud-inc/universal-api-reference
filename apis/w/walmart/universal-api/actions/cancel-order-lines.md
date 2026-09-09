# Walmart: Cancel Order Lines

Cancel one or more order lines for a specific `purchaseOrderId`.

```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/cancel-order-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/cancel-order-lines" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaseOrderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/cancel-order-lines', {
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
| `userInputLines[].lineNumber` | string | no | Identifier of the specific order line to be cancelled. |
| `userInputLines[]` | array<object> | no | Array of objects, each specifying cancellation details for an individual order line. |
| `userInputLines[].unitOfMeasurement` | list<string> | no | Unit of measure for the status quantity (such as EACH or EA), defining how the `amount` is counted. |
| `userInputLines[].amount` | number | no | Numeric value representing how many units to be cancelled. |
| `userInputLines[].cancellationReason` | list<string> | no | Reason for cancellation. Example: 'CUSTOMER_REQUESTED_SELLER_TO_CANCEL'. Cancellation reason should not be "CUSTOMER_REQUESTED_SELLER_TO_CANCEL" for non intent to cancel orders' Cancellation reason should not be "SELLER_CANCEL_FRAUD_STOP_SHIPMENT" for non fraudulent orders. If you suspect fraud, contact Walmart Risk Prevention Team (MPFraudReq@customercare.walmart.com). Include PO details and reason you suspect the order. We will contact you in 2-4 hours. If your suspicion of fraud is proven, we will cancel the order and notify you. If you select the cancellation reason as "SELLER_CANCEL_OUT_OF_STOCK", Walmart will mark the specific item as out of stock in the selected warehouse. To make the item available for sale again, please replenish its inventory. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dynamicSandbox` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerEmailId": "ava@example.com",
      "customerOrderId": "string",
      "orderDate": "string",
      "orderLines": {
        "orderLine": [
          {
            "charges": {
              "charge": [
                {
                  "chargeAmount": {
                    "amount": "string",
                    "currency": "string"
                  },
                  "chargeName": "Ava Chen",
                  "chargeType": "string",
                  "tax": {
                    "taxAmount": {
                      "amount": "string",
                      "currency": "string"
                    },
                    "taxName": "Ava Chen"
                  }
                }
              ]
            },
            "fulfillment": {
              "fulfillmentOption": "string",
              "pickUpDateTime": "string",
              "shipMethod": "string"
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
                  "status": "string",
                  "statusQuantity": {
                    "amount": "string",
                    "unitOfMeasurement": "string"
                  }
                }
              ]
            },
            "statusDate": "string"
          }
        ]
      },
      "orderType": "string",
      "purchaseOrderId": "string",
      "shippingInfo": {
        "estimatedDeliveryDate": "string",
        "estimatedShipDate": "string",
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
| `orderDate` | string |  |
| `orderLines.orderLine[].charges.charge[].chargeAmount.amount` | string |  |
| `orderLines.orderLine[].charges.charge[].chargeAmount.currency` | string |  |
| `orderLines.orderLine[].charges.charge[].chargeName` | string |  |
| `orderLines.orderLine[].charges.charge[].chargeType` | string |  |
| `orderLines.orderLine[].charges.charge[].tax.taxAmount.amount` | string |  |
| `orderLines.orderLine[].charges.charge[].tax.taxAmount.currency` | string |  |
| `orderLines.orderLine[].charges.charge[].tax.taxName` | string |  |
| `orderLines.orderLine[].fulfillment.fulfillmentOption` | string |  |
| `orderLines.orderLine[].fulfillment.pickUpDateTime` | string |  |
| `orderLines.orderLine[].fulfillment.shipMethod` | string |  |
| `orderLines.orderLine[].item.productName` | string |  |
| `orderLines.orderLine[].item.sku` | string |  |
| `orderLines.orderLine[].lineNumber` | string |  |
| `orderLines.orderLine[].orderLineQuantity.amount` | string |  |
| `orderLines.orderLine[].orderLineQuantity.unitOfMeasurement` | string |  |
| `orderLines.orderLine[].orderLineStatuses.orderLineStatus[].status` | string |  |
| `orderLines.orderLine[].orderLineStatuses.orderLineStatus[].statusQuantity.amount` | string |  |
| `orderLines.orderLine[].orderLineStatuses.orderLineStatus[].statusQuantity.unitOfMeasurement` | string |  |
| `orderLines.orderLine[].statusDate` | string |  |
| `orderType` | string |  |
| `purchaseOrderId` | string |  |
| `shippingInfo.estimatedDeliveryDate` | string |  |
| `shippingInfo.estimatedShipDate` | string |  |
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

Through the native Walmart API, this operation is `POST /v3/orders/:purchaseOrderId/cancel` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-order-lines.md) for the provider-specific parameters and requirements.

