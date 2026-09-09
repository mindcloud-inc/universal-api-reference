# Walmart: List Orders

Retrieves details of all orders with optional search criteria.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-all-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-all-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-all-orders?${params}`, {
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
| `customerOrderId` | string | no |  |
| `purchaseOrderId` | string | no |  |
| `sku` | string | no |  |
| `orderType` | list<string> | no | Filter by order type. Valid values are REGULAR, REPLACEMENT, PREORDER. Replacement orders appear only if replacementInfo is true. |
| `status` | list<string> | no | Status of purchase order line. Valid statuses are: Created, Acknowledged, Shipped, Delivered and Cancelled. Accepts multiple values as an array. |
| `shipNode` | list<string> | no | Filter by fulfillment node type. Valid values are SellerFulfilled, WFSFulfilled, and 3PLFulfilled. Default is SellerFulfilled. |
| `shippingProgramType` | list<string> | no | Filter by shipping program. Valid values are TWO_DAY or ONE_DAY. |
| `productInfo` | boolean | no |  |
| `serviceInfo` | boolean | no |  |
| `replacementInfo` | boolean | no | Include replacement order attributes (originalCustomerOrderID, orderType) in the response when true. Valid values are true or false. |
| `createdStartDate` | string | no |  |
| `createdEndDate` | string | no |  |
| `fromExpectedShipDate` | string | no |  |
| `toExpectedShipDate` | string | no |  |
| `lastModifiedStartDate` | string | no |  |
| `lastModifiedEndDate` | string | no |  |
| `isDynamicSandbox` | boolean | no |  |

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
      "originalCustomerOrderID": "string",
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
          "address2": "string",
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
| `originalCustomerOrderID` | string |  |
| `purchaseOrderId` | string |  |
| `shipNode.type` | string |  |
| `shippingInfo.estimatedDeliveryDate` | date |  |
| `shippingInfo.estimatedShipDate` | date |  |
| `shippingInfo.methodCode` | string |  |
| `shippingInfo.phone` | string |  |
| `shippingInfo.postalAddress.address1` | string |  |
| `shippingInfo.postalAddress.address2` | string |  |
| `shippingInfo.postalAddress.addressType` | string |  |
| `shippingInfo.postalAddress.city` | string |  |
| `shippingInfo.postalAddress.country` | string |  |
| `shippingInfo.postalAddress.name` | string |  |
| `shippingInfo.postalAddress.postalCode` | string |  |
| `shippingInfo.postalAddress.state` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/orders` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-orders.md) for the provider-specific parameters and requirements.

