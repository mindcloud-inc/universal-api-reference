# Webshipper: Create Order

Creates an order in Webshipper.

```
POST https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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
        "createdAt": "string",
        "createShipmentAutomatically": true,
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
        "dropPoint": {},
        "errorClass": {},
        "errorMessage": {},
        "externalComment": {},
        "extRef": {},
        "internalComment": {},
        "labelPrinted": {},
        "latestActivity": {},
        "latestStatusEvent": {},
        "lockState": {},
        "orderChannelId": 1,
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
            "packageId": {},
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
        "originalShipping": {},
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
        "shippingRateId": 1,
        "slipPrinted": {},
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
        "updatedAt": "string",
        "visibleRef": "string"
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
        "comments": {
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
        "errorType": {
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
        "orderChannel": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "packages": {
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
        "printJobs": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "returns": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "shipments": {
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
| `attributes.createdAt` | string |  |
| `attributes.createShipmentAutomatically` | boolean |  |
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
| `attributes.dropPoint` | object |  |
| `attributes.errorClass` | object |  |
| `attributes.errorMessage` | object |  |
| `attributes.externalComment` | object |  |
| `attributes.extRef` | object |  |
| `attributes.internalComment` | object |  |
| `attributes.labelPrinted` | object |  |
| `attributes.latestActivity` | object |  |
| `attributes.latestStatusEvent` | object |  |
| `attributes.lockState` | object |  |
| `attributes.orderChannelId` | number |  |
| `attributes.orderLines[].countryOfOrigin` | object |  |
| `attributes.orderLines[].createdAt` | string |  |
| `attributes.orderLines[].description` | string |  |
| `attributes.orderLines[].discountedUnitPrice` | number |  |
| `attributes.orderLines[].discountType` | string |  |
| `attributes.orderLines[].discountValue` | number |  |
| `attributes.orderLines[].extRef` | object |  |
| `attributes.orderLines[].id` | number |  |
| `attributes.orderLines[].isVirtual` | boolean |  |
| `attributes.orderLines[].location` | object |  |
| `attributes.orderLines[].orderId` | number |  |
| `attributes.orderLines[].packageId` | object |  |
| `attributes.orderLines[].quantity` | number |  |
| `attributes.orderLines[].sku` | string |  |
| `attributes.orderLines[].status` | string |  |
| `attributes.orderLines[].tarifNumber` | object |  |
| `attributes.orderLines[].unitPrice` | number |  |
| `attributes.orderLines[].updatedAt` | string |  |
| `attributes.orderLines[].vatPercent` | object |  |
| `attributes.orderLines[].weight` | number |  |
| `attributes.orderLines[].weightUnit` | string |  |
| `attributes.originalShipping` | object |  |
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
| `attributes.shippingRateId` | number |  |
| `attributes.slipPrinted` | object |  |
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
| `attributes.updatedAt` | string |  |
| `attributes.visibleRef` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.copyright` | string |  |
| `relationships.activities.links.related` | string |  |
| `relationships.activities.links.self` | string |  |
| `relationships.additionalAttributes.links.related` | string |  |
| `relationships.additionalAttributes.links.self` | string |  |
| `relationships.attachments.links.related` | string |  |
| `relationships.attachments.links.self` | string |  |
| `relationships.comments.links.related` | string |  |
| `relationships.comments.links.self` | string |  |
| `relationships.documents.links.related` | string |  |
| `relationships.documents.links.self` | string |  |
| `relationships.errorType.links.related` | string |  |
| `relationships.errorType.links.self` | string |  |
| `relationships.events.links.related` | string |  |
| `relationships.events.links.self` | string |  |
| `relationships.orderChannel.links.related` | string |  |
| `relationships.orderChannel.links.self` | string |  |
| `relationships.packages.links.related` | string |  |
| `relationships.packages.links.self` | string |  |
| `relationships.printerClient.links.related` | string |  |
| `relationships.printerClient.links.self` | string |  |
| `relationships.printJobs.links.related` | string |  |
| `relationships.printJobs.links.self` | string |  |
| `relationships.returns.links.related` | string |  |
| `relationships.returns.links.self` | string |  |
| `relationships.shipments.links.related` | string |  |
| `relationships.shipments.links.self` | string |  |
| `relationships.shippingRate.links.related` | string |  |
| `relationships.shippingRate.links.self` | string |  |
| `relationships.statusEvents.links.related` | string |  |
| `relationships.statusEvents.links.self` | string |  |
| `relationships.stores.links.related` | string |  |
| `relationships.stores.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `POST /orders` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

