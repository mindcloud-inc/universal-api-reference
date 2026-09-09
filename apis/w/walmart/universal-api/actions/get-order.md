# Walmart: Get Order

Retrieves an order detail for a specific purchaseOrderId

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-order?connectionId=$CONNECTION_ID&purchaseOrderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchaseOrderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-order?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productInfo` | boolean | no |  |
| `purchaseOrderId` | string | yes | Unique Walmart purchaseOrderId that identifies the purchase order. |
| `replacementInfo` | boolean | no | Include replacement order attributes (originalCustomerOrderID, orderType) in the response when true. Valid values are true or false. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dynamicSandbox` | boolean | no | - When Toggled Off and credential is set to 'Sandbox' - this request will return a static Walmart Sandbox Order. - Toggle on to fetch an Order from your Dynamic Sandbox ( created via the SImulations API. ) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerEmailId": "ava@example.com",
      "customerOrderId": "string",
      "orderDate": "2026-05-07T12:00:00.000Z",
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
              "pickUpDateTime": "2026-05-07T12:00:00.000Z",
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
            }
          }
        ],
        "orderLine[0]": {
          "statusDate": "2026-05-07T12:00:00.000Z"
        }
      },
      "purchaseOrderId": "string",
      "shipNode": {
        "type": "string"
      },
      "shippingInfo": {
        "estimatedDeliveryDate": "2026-05-07T12:00:00.000Z",
        "estimatedShipDate": "2026-05-07T12:00:00.000Z",
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
| `orderDate` | date |  |
| `orderLines.orderLine[].charges.charge[].chargeAmount.amount` | number |  |
| `orderLines.orderLine[].charges.charge[].chargeAmount.currency` | string |  |
| `orderLines.orderLine[].charges.charge[].chargeName` | string |  |
| `orderLines.orderLine[].charges.charge[].chargeType` | string |  |
| `orderLines.orderLine[].charges.charge[].tax.taxAmount.amount` | number |  |
| `orderLines.orderLine[].charges.charge[].tax.taxAmount.currency` | string |  |
| `orderLines.orderLine[].charges.charge[].tax.taxName` | string |  |
| `orderLines.orderLine[].fulfillment.fulfillmentOption` | string |  |
| `orderLines.orderLine[].fulfillment.pickUpDateTime` | date |  |
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
| `orderLines.orderLine[0].statusDate` | date |  |
| `purchaseOrderId` | string |  |
| `shipNode.type` | string |  |
| `shippingInfo.estimatedDeliveryDate` | date |  |
| `shippingInfo.estimatedShipDate` | date |  |
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

Through the native Walmart API, this operation is `GET /v3/orders/:purchaseOrderId` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

