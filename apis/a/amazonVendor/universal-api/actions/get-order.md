# Amazon Vendor: Get Order



```
GET https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Vendor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-order?connectionId=$CONNECTION_ID&purchaseOrderNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchaseOrderNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-order?${params}`, {
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
| `purchaseOrderNumber` | string | yes | The alphanumeric identifier of the purchase order to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderDetails": {
        "billToParty": {
          "partyId": "string"
        },
        "customerOrderNumber": "string",
        "hasCustomizableItems": true,
        "items": [
          [
            {}
          ]
        ],
        "orderDate": "string",
        "orderStatus": "string",
        "sellingParty": {
          "partyId": "string"
        },
        "shipFromParty": {
          "partyId": "string"
        },
        "shipmentDetails": {
          "isGift": true,
          "isPriorityShipment": true,
          "isPslipRequired": true,
          "isScheduledDeliveryShipment": true,
          "shipmentDates": {
            "promisedDeliveryDate": "string",
            "requiredShipDate": "string"
          },
          "shipMethod": "string"
        },
        "shipToParty": {
          "addressLine1": "string",
          "addressLine2": "string",
          "addressLine3": "string",
          "city": "string",
          "countryCode": "string",
          "county": "string",
          "name": "Ava Chen",
          "phone": "string",
          "postalCode": "string",
          "stateOrRegion": "string"
        },
        "taxTotal": {
          "taxLineItem": [
            [
              {}
            ]
          ]
        }
      },
      "purchaseOrderNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderDetails` | object |  |
| `orderDetails.billToParty` | object |  |
| `orderDetails.billToParty.partyId` | string |  |
| `orderDetails.customerOrderNumber` | string |  |
| `orderDetails.hasCustomizableItems` | boolean |  |
| `orderDetails.items[]` | array<object> |  |
| `orderDetails.items[].buyerProductIdentifier` | string |  |
| `orderDetails.items[].itemSequenceNumber` | number |  |
| `orderDetails.items[].netPrice` | object |  |
| `orderDetails.items[].netPrice.amount` | string |  |
| `orderDetails.items[].netPrice.currencyCode` | string |  |
| `orderDetails.items[].orderedQuantity` | object |  |
| `orderDetails.items[].orderedQuantity.amount` | number |  |
| `orderDetails.items[].orderedQuantity.unitOfMeasure` | string |  |
| `orderDetails.items[].taxDetails` | object |  |
| `orderDetails.items[].taxDetails.taxLineItem[]` | array<object> |  |
| `orderDetails.items[].taxDetails.taxLineItem[].taxAmount` | object |  |
| `orderDetails.items[].taxDetails.taxLineItem[].taxAmount.amount` | string |  |
| `orderDetails.items[].taxDetails.taxLineItem[].taxAmount.currencyCode` | string |  |
| `orderDetails.items[].taxDetails.taxLineItem[].taxRate` | string |  |
| `orderDetails.items[].title` | string |  |
| `orderDetails.items[].totalPrice` | object |  |
| `orderDetails.items[].totalPrice.amount` | string |  |
| `orderDetails.items[].totalPrice.currencyCode` | string |  |
| `orderDetails.items[].vendorProductIdentifier` | string |  |
| `orderDetails.orderDate` | string |  |
| `orderDetails.orderStatus` | string |  |
| `orderDetails.sellingParty` | object |  |
| `orderDetails.sellingParty.partyId` | string |  |
| `orderDetails.shipFromParty` | object |  |
| `orderDetails.shipFromParty.partyId` | string |  |
| `orderDetails.shipmentDetails` | object |  |
| `orderDetails.shipmentDetails.isGift` | boolean |  |
| `orderDetails.shipmentDetails.isPriorityShipment` | boolean |  |
| `orderDetails.shipmentDetails.isPslipRequired` | boolean |  |
| `orderDetails.shipmentDetails.isScheduledDeliveryShipment` | boolean |  |
| `orderDetails.shipmentDetails.shipmentDates` | object |  |
| `orderDetails.shipmentDetails.shipmentDates.promisedDeliveryDate` | string |  |
| `orderDetails.shipmentDetails.shipmentDates.requiredShipDate` | string |  |
| `orderDetails.shipmentDetails.shipMethod` | string |  |
| `orderDetails.shipToParty` | object |  |
| `orderDetails.shipToParty.addressLine1` | string |  |
| `orderDetails.shipToParty.addressLine2` | string |  |
| `orderDetails.shipToParty.addressLine3` | string |  |
| `orderDetails.shipToParty.city` | string |  |
| `orderDetails.shipToParty.countryCode` | string |  |
| `orderDetails.shipToParty.county` | string |  |
| `orderDetails.shipToParty.name` | string |  |
| `orderDetails.shipToParty.phone` | string |  |
| `orderDetails.shipToParty.postalCode` | string |  |
| `orderDetails.shipToParty.stateOrRegion` | string |  |
| `orderDetails.taxTotal` | object |  |
| `orderDetails.taxTotal.taxLineItem[]` | array<object> |  |
| `orderDetails.taxTotal.taxLineItem[].taxAmount` | object |  |
| `orderDetails.taxTotal.taxLineItem[].taxAmount.amount` | string |  |
| `orderDetails.taxTotal.taxLineItem[].taxAmount.currencyCode` | string |  |
| `purchaseOrderNumber` | string |  |

## Native endpoint

Through the native Amazon Vendor API, this operation is `GET /vendor/directFulfillment/orders/2021-12-28/purchaseOrders/:purchaseOrderNumber` (base URL `https://sellingpartnerapi-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

