# Webshipper Universal API Examples

These examples use the MindCloud API key and Webshipper connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Order Channel Types

Retrieves order channel types from Webshipper.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-order-channel-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-order-channel-types?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "canAutofulfill": true,
        "canLimitDropPoints": true,
        "description": "string",
        "hide": true,
        "listLogo": "string",
        "moduleLink": "https://example.com",
        "name": "Ava Chen",
        "supportsIdImport": true,
        "supportsRateQuoting": true,
        "supportsStatusesImport": true,
        "supportsTimeIntervalImport": true,
        "supportsVatInCheckout": true,
        "supportUrl": "https://example.com",
        "usesScheduledImport": true
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "copyright": "string"
      },
      "relationships": {
        "localAttrs": {
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

See the full [List Order Channel Types action reference](actions/list-order-channel-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webshipper/latest/actions/list-order-channel-types).

## Create Order

Creates an order in Webshipper.

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

Example response:

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

See the full [Create Order action reference](actions/create-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webshipper/latest/actions/create-order).
