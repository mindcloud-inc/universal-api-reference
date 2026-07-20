# Webshipper: Create Shipment

Creates a shipment in Webshipper.

```
POST https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.relationships.order.data.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.relationships.order.data.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.relationships.order.data.id` | string | yes | Order ID to create the shipment from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "billingAddress": {
          "address1": "string",
          "address2": {},
          "addressType": "string",
          "attContact": {},
          "city": "string",
          "companyName": "Ava Chen",
          "countryCode": "string",
          "createdAt": "string",
          "duns": {},
          "email": {},
          "eori": {},
          "extLocation": {},
          "fda": {},
          "formattedRecipient": "string",
          "id": 1,
          "ioss": {},
          "personalCustomsNo": {},
          "phone": {},
          "sprn": {},
          "state": {},
          "updatedAt": "string",
          "vatNo": {},
          "voec": {},
          "zip": "string"
        },
        "carrierAlias": "string",
        "carrierId": 1,
        "carrierTypeName": "Ava Chen",
        "comment": "string",
        "costPrice": {},
        "createdAt": "string",
        "csvUploadId": {},
        "currency": "string",
        "deliveryAddress": {
          "address1": "string",
          "address2": {},
          "addressType": "string",
          "attContact": {},
          "city": "string",
          "companyName": "Ava Chen",
          "countryCode": "string",
          "createdAt": "string",
          "duns": {},
          "email": {},
          "eori": {},
          "extLocation": {},
          "fda": {},
          "formattedRecipient": "string",
          "id": 1,
          "ioss": {},
          "personalCustomsNo": {},
          "phone": {},
          "sprn": {},
          "state": {},
          "updatedAt": "string",
          "vatNo": {},
          "voec": {},
          "zip": "string"
        },
        "documentTemplate": {},
        "dropPoint": {},
        "dutiable": {},
        "emailNotification": {},
        "extRef": {},
        "fulfillImmediately": true,
        "invoiceSettings": {},
        "isReturn": {},
        "latestActivity": {},
        "latestStatusEvent": {},
        "latestUpdateTime": {},
        "manualOrderShipmentCreation": true,
        "omitPrint": true,
        "originalShipmentId": {},
        "packages": [
          {
            "barcodeUsageId": {},
            "barcodeUsageType": {},
            "colliType": {},
            "createdAt": "string",
            "customsLines": [
              {
                "countryOfOrigin": {},
                "createdAt": "string",
                "currency": "string",
                "description": "string",
                "discount": 1,
                "extRef": {},
                "id": 1,
                "packageId": 1,
                "quantity": 1,
                "sku": "string",
                "tarifNumber": {},
                "unitPrice": 1,
                "updatedAt": "string",
                "vatPercent": 1,
                "weight": 1,
                "weightUnit": "string"
              }
            ],
            "extRef": {},
            "id": 1,
            "labellessCode": {},
            "orderLines": [
              {
                "countryOfOrigin": {},
                "createdAt": "string",
                "description": "string",
                "discountedUnitPrice": 1,
                "discountType": "string",
                "discountValue": 1,
                "extRef": {},
                "id": 1,
                "isVirtual": true,
                "location": {},
                "orderId": 1,
                "packageId": 1,
                "quantity": 1,
                "sku": "string",
                "status": "string",
                "tarifNumber": {},
                "unitPrice": 1,
                "updatedAt": "string",
                "vatPercent": {},
                "weight": 1,
                "weightUnit": "string"
              }
            ],
            "shipmentId": 1,
            "updatedAt": "string",
            "weight": 1,
            "weightUnit": "string"
          }
        ],
        "pickupAddress": {
          "address1": "string",
          "address2": {},
          "addressType": "string",
          "attContact": {},
          "city": "string",
          "companyName": "Ava Chen",
          "countryCode": "string",
          "createdAt": "string",
          "duns": {},
          "email": {},
          "eori": {},
          "extLocation": {},
          "fda": {},
          "formattedRecipient": "string",
          "id": 1,
          "ioss": {},
          "personalCustomsNo": {},
          "phone": {},
          "sprn": {},
          "state": {},
          "updatedAt": "string",
          "vatNo": {},
          "voec": {},
          "zip": "string"
        },
        "reference": "string",
        "returnAddress": {
          "address1": "string",
          "address2": {},
          "addressType": "string",
          "attContact": {},
          "city": "string",
          "companyName": "Ava Chen",
          "countryCode": "string",
          "createdAt": "string",
          "duns": {},
          "email": {},
          "eori": {},
          "extLocation": {},
          "fda": {},
          "formattedRecipient": "string",
          "id": 1,
          "ioss": {},
          "personalCustomsNo": {},
          "phone": {},
          "sprn": {},
          "state": {},
          "updatedAt": "string",
          "vatNo": {},
          "voec": {},
          "zip": "string"
        },
        "salesPrice": {},
        "senderAddress": {
          "address1": "string",
          "address2": {},
          "addressType": "string",
          "attContact": {},
          "city": "string",
          "companyName": "Ava Chen",
          "countryCode": "string",
          "createdAt": "string",
          "duns": {},
          "email": {},
          "eori": {},
          "extLocation": {},
          "fda": {},
          "formattedRecipient": "string",
          "id": 1,
          "ioss": {},
          "personalCustomsNo": {},
          "phone": {},
          "sprn": {},
          "state": {},
          "updatedAt": "string",
          "vatNo": {},
          "voec": {},
          "zip": "string"
        },
        "sendTime": "string",
        "serviceCode": "string",
        "shadowBookingAsParent": {},
        "smsNotification": {},
        "soldFromAddress": {
          "address1": "string",
          "address2": {},
          "addressType": "string",
          "attContact": {},
          "city": "string",
          "companyName": "Ava Chen",
          "countryCode": "string",
          "createdAt": "string",
          "duns": {},
          "email": {},
          "eori": {},
          "extLocation": {},
          "fda": {},
          "formattedRecipient": "string",
          "id": 1,
          "ioss": {},
          "personalCustomsNo": {},
          "phone": {},
          "sprn": {},
          "state": {},
          "updatedAt": "string",
          "vatNo": {},
          "voec": {},
          "zip": "string"
        },
        "source": "string",
        "status": "string",
        "supportsUpdates": true,
        "testMode": true
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "copyright": "string"
      },
      "relationships": {
        "activities": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "additionalAttributes": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "attachments": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "carrier": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "documents": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "documentTemplate": {
          "data": {},
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "edis": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "events": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "labels": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "mailTemplate": {
          "data": {},
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "order": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "originalShipment": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "pickup": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "printerClient": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "return": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "returnLabelMailTemplate": {
          "data": {},
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "returnShipments": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "shadowShipment": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "shippingRate": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "statusEvents": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "stores": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.billingAddress.address1` | string |  |
| `attributes.billingAddress.address2` | object |  |
| `attributes.billingAddress.addressType` | string |  |
| `attributes.billingAddress.attContact` | object |  |
| `attributes.billingAddress.city` | string |  |
| `attributes.billingAddress.companyName` | string |  |
| `attributes.billingAddress.countryCode` | string |  |
| `attributes.billingAddress.createdAt` | string |  |
| `attributes.billingAddress.duns` | object |  |
| `attributes.billingAddress.email` | object |  |
| `attributes.billingAddress.eori` | object |  |
| `attributes.billingAddress.extLocation` | object |  |
| `attributes.billingAddress.fda` | object |  |
| `attributes.billingAddress.formattedRecipient` | string |  |
| `attributes.billingAddress.id` | number |  |
| `attributes.billingAddress.ioss` | object |  |
| `attributes.billingAddress.personalCustomsNo` | object |  |
| `attributes.billingAddress.phone` | object |  |
| `attributes.billingAddress.sprn` | object |  |
| `attributes.billingAddress.state` | object |  |
| `attributes.billingAddress.updatedAt` | string |  |
| `attributes.billingAddress.vatNo` | object |  |
| `attributes.billingAddress.voec` | object |  |
| `attributes.billingAddress.zip` | string |  |
| `attributes.carrierAlias` | string |  |
| `attributes.carrierId` | number |  |
| `attributes.carrierTypeName` | string |  |
| `attributes.comment` | string |  |
| `attributes.costPrice` | object |  |
| `attributes.createdAt` | string |  |
| `attributes.csvUploadId` | object |  |
| `attributes.currency` | string |  |
| `attributes.deliveryAddress.address1` | string |  |
| `attributes.deliveryAddress.address2` | object |  |
| `attributes.deliveryAddress.addressType` | string |  |
| `attributes.deliveryAddress.attContact` | object |  |
| `attributes.deliveryAddress.city` | string |  |
| `attributes.deliveryAddress.companyName` | string |  |
| `attributes.deliveryAddress.countryCode` | string |  |
| `attributes.deliveryAddress.createdAt` | string |  |
| `attributes.deliveryAddress.duns` | object |  |
| `attributes.deliveryAddress.email` | object |  |
| `attributes.deliveryAddress.eori` | object |  |
| `attributes.deliveryAddress.extLocation` | object |  |
| `attributes.deliveryAddress.fda` | object |  |
| `attributes.deliveryAddress.formattedRecipient` | string |  |
| `attributes.deliveryAddress.id` | number |  |
| `attributes.deliveryAddress.ioss` | object |  |
| `attributes.deliveryAddress.personalCustomsNo` | object |  |
| `attributes.deliveryAddress.phone` | object |  |
| `attributes.deliveryAddress.sprn` | object |  |
| `attributes.deliveryAddress.state` | object |  |
| `attributes.deliveryAddress.updatedAt` | string |  |
| `attributes.deliveryAddress.vatNo` | object |  |
| `attributes.deliveryAddress.voec` | object |  |
| `attributes.deliveryAddress.zip` | string |  |
| `attributes.documentTemplate` | object |  |
| `attributes.dropPoint` | object |  |
| `attributes.dutiable` | object |  |
| `attributes.emailNotification` | object |  |
| `attributes.extRef` | object |  |
| `attributes.fulfillImmediately` | boolean |  |
| `attributes.invoiceSettings` | object |  |
| `attributes.isReturn` | object |  |
| `attributes.latestActivity` | object |  |
| `attributes.latestStatusEvent` | object |  |
| `attributes.latestUpdateTime` | object |  |
| `attributes.manualOrderShipmentCreation` | boolean |  |
| `attributes.omitPrint` | boolean |  |
| `attributes.originalShipmentId` | object |  |
| `attributes.packages[].barcodeUsageId` | object |  |
| `attributes.packages[].barcodeUsageType` | object |  |
| `attributes.packages[].colliType` | object |  |
| `attributes.packages[].createdAt` | string |  |
| `attributes.packages[].customsLines[].countryOfOrigin` | object |  |
| `attributes.packages[].customsLines[].createdAt` | string |  |
| `attributes.packages[].customsLines[].currency` | string |  |
| `attributes.packages[].customsLines[].description` | string |  |
| `attributes.packages[].customsLines[].discount` | number |  |
| `attributes.packages[].customsLines[].extRef` | object |  |
| `attributes.packages[].customsLines[].id` | number |  |
| `attributes.packages[].customsLines[].packageId` | number |  |
| `attributes.packages[].customsLines[].quantity` | number |  |
| `attributes.packages[].customsLines[].sku` | string |  |
| `attributes.packages[].customsLines[].tarifNumber` | object |  |
| `attributes.packages[].customsLines[].unitPrice` | number |  |
| `attributes.packages[].customsLines[].updatedAt` | string |  |
| `attributes.packages[].customsLines[].vatPercent` | number |  |
| `attributes.packages[].customsLines[].weight` | number |  |
| `attributes.packages[].customsLines[].weightUnit` | string |  |
| `attributes.packages[].extRef` | object |  |
| `attributes.packages[].id` | number |  |
| `attributes.packages[].labellessCode` | object |  |
| `attributes.packages[].orderLines[].countryOfOrigin` | object |  |
| `attributes.packages[].orderLines[].createdAt` | string |  |
| `attributes.packages[].orderLines[].description` | string |  |
| `attributes.packages[].orderLines[].discountedUnitPrice` | number |  |
| `attributes.packages[].orderLines[].discountType` | string |  |
| `attributes.packages[].orderLines[].discountValue` | number |  |
| `attributes.packages[].orderLines[].extRef` | object |  |
| `attributes.packages[].orderLines[].id` | number |  |
| `attributes.packages[].orderLines[].isVirtual` | boolean |  |
| `attributes.packages[].orderLines[].location` | object |  |
| `attributes.packages[].orderLines[].orderId` | number |  |
| `attributes.packages[].orderLines[].packageId` | number |  |
| `attributes.packages[].orderLines[].quantity` | number |  |
| `attributes.packages[].orderLines[].sku` | string |  |
| `attributes.packages[].orderLines[].status` | string |  |
| `attributes.packages[].orderLines[].tarifNumber` | object |  |
| `attributes.packages[].orderLines[].unitPrice` | number |  |
| `attributes.packages[].orderLines[].updatedAt` | string |  |
| `attributes.packages[].orderLines[].vatPercent` | object |  |
| `attributes.packages[].orderLines[].weight` | number |  |
| `attributes.packages[].orderLines[].weightUnit` | string |  |
| `attributes.packages[].shipmentId` | number |  |
| `attributes.packages[].updatedAt` | string |  |
| `attributes.packages[].weight` | number |  |
| `attributes.packages[].weightUnit` | string |  |
| `attributes.pickupAddress.address1` | string |  |
| `attributes.pickupAddress.address2` | object |  |
| `attributes.pickupAddress.addressType` | string |  |
| `attributes.pickupAddress.attContact` | object |  |
| `attributes.pickupAddress.city` | string |  |
| `attributes.pickupAddress.companyName` | string |  |
| `attributes.pickupAddress.countryCode` | string |  |
| `attributes.pickupAddress.createdAt` | string |  |
| `attributes.pickupAddress.duns` | object |  |
| `attributes.pickupAddress.email` | object |  |
| `attributes.pickupAddress.eori` | object |  |
| `attributes.pickupAddress.extLocation` | object |  |
| `attributes.pickupAddress.fda` | object |  |
| `attributes.pickupAddress.formattedRecipient` | string |  |
| `attributes.pickupAddress.id` | number |  |
| `attributes.pickupAddress.ioss` | object |  |
| `attributes.pickupAddress.personalCustomsNo` | object |  |
| `attributes.pickupAddress.phone` | object |  |
| `attributes.pickupAddress.sprn` | object |  |
| `attributes.pickupAddress.state` | object |  |
| `attributes.pickupAddress.updatedAt` | string |  |
| `attributes.pickupAddress.vatNo` | object |  |
| `attributes.pickupAddress.voec` | object |  |
| `attributes.pickupAddress.zip` | string |  |
| `attributes.reference` | string |  |
| `attributes.returnAddress.address1` | string |  |
| `attributes.returnAddress.address2` | object |  |
| `attributes.returnAddress.addressType` | string |  |
| `attributes.returnAddress.attContact` | object |  |
| `attributes.returnAddress.city` | string |  |
| `attributes.returnAddress.companyName` | string |  |
| `attributes.returnAddress.countryCode` | string |  |
| `attributes.returnAddress.createdAt` | string |  |
| `attributes.returnAddress.duns` | object |  |
| `attributes.returnAddress.email` | object |  |
| `attributes.returnAddress.eori` | object |  |
| `attributes.returnAddress.extLocation` | object |  |
| `attributes.returnAddress.fda` | object |  |
| `attributes.returnAddress.formattedRecipient` | string |  |
| `attributes.returnAddress.id` | number |  |
| `attributes.returnAddress.ioss` | object |  |
| `attributes.returnAddress.personalCustomsNo` | object |  |
| `attributes.returnAddress.phone` | object |  |
| `attributes.returnAddress.sprn` | object |  |
| `attributes.returnAddress.state` | object |  |
| `attributes.returnAddress.updatedAt` | string |  |
| `attributes.returnAddress.vatNo` | object |  |
| `attributes.returnAddress.voec` | object |  |
| `attributes.returnAddress.zip` | string |  |
| `attributes.salesPrice` | object |  |
| `attributes.senderAddress.address1` | string |  |
| `attributes.senderAddress.address2` | object |  |
| `attributes.senderAddress.addressType` | string |  |
| `attributes.senderAddress.attContact` | object |  |
| `attributes.senderAddress.city` | string |  |
| `attributes.senderAddress.companyName` | string |  |
| `attributes.senderAddress.countryCode` | string |  |
| `attributes.senderAddress.createdAt` | string |  |
| `attributes.senderAddress.duns` | object |  |
| `attributes.senderAddress.email` | object |  |
| `attributes.senderAddress.eori` | object |  |
| `attributes.senderAddress.extLocation` | object |  |
| `attributes.senderAddress.fda` | object |  |
| `attributes.senderAddress.formattedRecipient` | string |  |
| `attributes.senderAddress.id` | number |  |
| `attributes.senderAddress.ioss` | object |  |
| `attributes.senderAddress.personalCustomsNo` | object |  |
| `attributes.senderAddress.phone` | object |  |
| `attributes.senderAddress.sprn` | object |  |
| `attributes.senderAddress.state` | object |  |
| `attributes.senderAddress.updatedAt` | string |  |
| `attributes.senderAddress.vatNo` | object |  |
| `attributes.senderAddress.voec` | object |  |
| `attributes.senderAddress.zip` | string |  |
| `attributes.sendTime` | string |  |
| `attributes.serviceCode` | string |  |
| `attributes.shadowBookingAsParent` | object |  |
| `attributes.smsNotification` | object |  |
| `attributes.soldFromAddress.address1` | string |  |
| `attributes.soldFromAddress.address2` | object |  |
| `attributes.soldFromAddress.addressType` | string |  |
| `attributes.soldFromAddress.attContact` | object |  |
| `attributes.soldFromAddress.city` | string |  |
| `attributes.soldFromAddress.companyName` | string |  |
| `attributes.soldFromAddress.countryCode` | string |  |
| `attributes.soldFromAddress.createdAt` | string |  |
| `attributes.soldFromAddress.duns` | object |  |
| `attributes.soldFromAddress.email` | object |  |
| `attributes.soldFromAddress.eori` | object |  |
| `attributes.soldFromAddress.extLocation` | object |  |
| `attributes.soldFromAddress.fda` | object |  |
| `attributes.soldFromAddress.formattedRecipient` | string |  |
| `attributes.soldFromAddress.id` | number |  |
| `attributes.soldFromAddress.ioss` | object |  |
| `attributes.soldFromAddress.personalCustomsNo` | object |  |
| `attributes.soldFromAddress.phone` | object |  |
| `attributes.soldFromAddress.sprn` | object |  |
| `attributes.soldFromAddress.state` | object |  |
| `attributes.soldFromAddress.updatedAt` | string |  |
| `attributes.soldFromAddress.vatNo` | object |  |
| `attributes.soldFromAddress.voec` | object |  |
| `attributes.soldFromAddress.zip` | string |  |
| `attributes.source` | string |  |
| `attributes.status` | string |  |
| `attributes.supportsUpdates` | boolean |  |
| `attributes.testMode` | boolean |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.copyright` | string |  |
| `relationships.activities.links.related` | string |  |
| `relationships.activities.links.self` | string |  |
| `relationships.additionalAttributes.links.related` | string |  |
| `relationships.additionalAttributes.links.self` | string |  |
| `relationships.attachments.links.related` | string |  |
| `relationships.attachments.links.self` | string |  |
| `relationships.carrier.links.related` | string |  |
| `relationships.carrier.links.self` | string |  |
| `relationships.documents.links.related` | string |  |
| `relationships.documents.links.self` | string |  |
| `relationships.documentTemplate.data` | object |  |
| `relationships.documentTemplate.links.related` | string |  |
| `relationships.documentTemplate.links.self` | string |  |
| `relationships.edis.links.related` | string |  |
| `relationships.edis.links.self` | string |  |
| `relationships.events.links.related` | string |  |
| `relationships.events.links.self` | string |  |
| `relationships.labels.links.related` | string |  |
| `relationships.labels.links.self` | string |  |
| `relationships.mailTemplate.data` | object |  |
| `relationships.mailTemplate.links.related` | string |  |
| `relationships.mailTemplate.links.self` | string |  |
| `relationships.order.links.related` | string |  |
| `relationships.order.links.self` | string |  |
| `relationships.originalShipment.links.related` | string |  |
| `relationships.originalShipment.links.self` | string |  |
| `relationships.pickup.links.related` | string |  |
| `relationships.pickup.links.self` | string |  |
| `relationships.printerClient.links.related` | string |  |
| `relationships.printerClient.links.self` | string |  |
| `relationships.return.links.related` | string |  |
| `relationships.return.links.self` | string |  |
| `relationships.returnLabelMailTemplate.data` | object |  |
| `relationships.returnLabelMailTemplate.links.related` | string |  |
| `relationships.returnLabelMailTemplate.links.self` | string |  |
| `relationships.returnShipments.links.related` | string |  |
| `relationships.returnShipments.links.self` | string |  |
| `relationships.shadowShipment.links.related` | string |  |
| `relationships.shadowShipment.links.self` | string |  |
| `relationships.shippingRate.links.related` | string |  |
| `relationships.shippingRate.links.self` | string |  |
| `relationships.statusEvents.links.related` | string |  |
| `relationships.statusEvents.links.self` | string |  |
| `relationships.stores.links.related` | string |  |
| `relationships.stores.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `POST /shipments` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment.md) for the provider-specific parameters and requirements.

