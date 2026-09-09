# Walmart: Ship Order Lines

Marks specified order lines in a single purchase order as shipped.

```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/ship-order-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/ship-order-lines" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaseOrderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/ship-order-lines', {
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
| `processMode` | string | no | Optional. If updating tracking info after shipment, set this fields value to: PARTIAL_UPDATE to indicate a partial update of shipping information. |
| `userInputLines[].lineNumber` | string | no | Identifier of the specific order line to be cancelled. |
| `userInputLines[].trackingInfo.carrier` | list<string> | no | The package shipment carrier. Valid entries are: UPS, USPS, FedEx, Airborne, OnTrac, DHL Ecommerce - US, DHL, LS (LaserShip), UDS (United Delivery Service), UPSMI (UPS Mail Innovations), FDX, PILOT, ESTES, SAIA, FDS Express, Seko Worldwide, HIT Delivery, FEDEXSP (FedEx SmartPost), RL Carriers, Metropolitan Warehouse & Delivery, China Post, YunExpress,Yellow Freight Sys, AIT Worldwide Logistics, Chukou1, Sendle, Landmark Global, Sunyou, Yanwen, 4PX, GLS, OSM Worldwide, FIRST MILE, AM Trucking, CEVA, India Post, SF Express, CNE, TForce Freight, AxleHire, LSO, Royal Mail, ABF Freight System, WanB, Roadrunner Freight, Meyer Distribution, AAA Cooper, Canada Post, Southeastern Freight Lines, Japan Post, Correos de Mexico, XPO Logistics, JD Logistics, YDH, JCEX, Flyt, Deutsche Post, Better Trucks, Asendia, SFC, UBI, ePost Global, YF Logistics, RXO, Estes Express, Shypmax, WIN.IT America, PITT OHIO, PostNord Sweden, Equick, Whistl, Tusou, Shiprocket, DTDC, PTS. |
| `userInputLines[]` | array<object> | no | Array of objects, each specifying cancellation details for an individual order line. |
| `userInputLines[].intentToCancelOverride` | boolean | no | Optional. If the customer has requested cancellation, toggle on to confirm you still intend to ship the order. Example: `False`. |
| `userInputLines[].trackingInfo.otherCarrier` | string | no | Custom name for a shipping carrier when the carrier is not one of the predefined options; if used, a valid trackingURL must also be provided. |
| `userInputLines[].sellerOrderId` | string | no | Seller-defined order ID (max 30 characters). Walmart prints this ID on return labels so the seller can reference the sales order. |
| `userInputLines[].trackingInfo.methodCode` | string | no | Shipping service level for the package (such as Standard, Express, OneDay, WhiteGlove, Value, Freight), indicating delivery speed or handling. |
| `userInputLines[].sellerOrderNo` | string | no | Seller’s unique purchase order number for this order, used internally when creating or updating orders. |
| `userInputLines[].trackingInfo.trackingNumber` | string | no | Current alphanumeric identifier assigned by the carrier, used to update the purchase order’s tracking status. |
| `userInputLines[].trackingInfo.trackingURL` | string | no | URL where the shipment status can be tracked online. Mandatory when using a custom otherCarrier name. |
| `userInputLines[].trackingInfo.shipDateTime` | date | no | Timestamp in UNIX epoch (int64) format representing the exact date and time the package was shipped. |
| `userInputLines[].unitOfMeasurement` | list<string> | no | Unit of measure for the status quantity (such as EACH or EA), defining how the amount is counted. |
| `userInputLines[].amount` | number | no | Numeric value representing how many units fall into the specified status category. |
| `userInputLines[].trackingInfo` | object | no | Object containing shipment and tracking details for the package, including carrier information, shipping method, shipment timestamp, tracking number, and optional tracking URL' |

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
      "originalCustomerOrderID": "string",
      "purchaseOrderId": "string",
      "shippingInfo": {
        "estimatedDeliveryDate": "string",
        "estimatedShipDate": "string",
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
| `originalCustomerOrderID` | string |  |
| `purchaseOrderId` | string |  |
| `shippingInfo.estimatedDeliveryDate` | string |  |
| `shippingInfo.estimatedShipDate` | string |  |
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

Through the native Walmart API, this operation is `POST /v3/orders/:purchaseOrderId/shipping` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ship-order-lines.md) for the provider-specific parameters and requirements.

