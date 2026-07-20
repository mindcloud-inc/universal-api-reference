# Webshipper: Create Shipping Rate

Creates a shipping rate in Webshipper.

```
POST https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-shipping-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-shipping-rate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-shipping-rate', {
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
        "carrierId": 1,
        "carriersEmail": {},
        "carrierServiceCode": "string",
        "carriersSms": {},
        "clickCollect": {},
        "commentMap": "string",
        "createdAt": "string",
        "customMessage": {},
        "defaultColliType": {},
        "dimensions": {},
        "dutiable": {},
        "ignoreRateQuoteValidation": true,
        "isHidden": true,
        "isReturn": {},
        "name": "Ava Chen",
        "orderChannelId": 1,
        "reference": {},
        "referenceMap": "string",
        "requireDropPoint": {},
        "returnAddressId": {},
        "senderAddressId": {},
        "shadowBookingKeepDocuments": {},
        "shadowBookingKeepLabels": {},
        "updatedAt": "string",
        "visibleFor": {}
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "copyright": "string"
      },
      "relationships": {
        "carrier": {
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
        "mailTemplate": {
          "data": {},
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
        "regions": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "returnAddress": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "returnMailTemplate": {
          "data": {},
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "returnShippingRate": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "senderAddress": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "shadowBookingShippingRate": {
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
| `attributes.carrierId` | number |  |
| `attributes.carriersEmail` | object |  |
| `attributes.carrierServiceCode` | string |  |
| `attributes.carriersSms` | object |  |
| `attributes.clickCollect` | object |  |
| `attributes.commentMap` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.customMessage` | object |  |
| `attributes.defaultColliType` | object |  |
| `attributes.dimensions` | object |  |
| `attributes.dutiable` | object |  |
| `attributes.ignoreRateQuoteValidation` | boolean |  |
| `attributes.isHidden` | boolean |  |
| `attributes.isReturn` | object |  |
| `attributes.name` | string |  |
| `attributes.orderChannelId` | number |  |
| `attributes.reference` | object |  |
| `attributes.referenceMap` | string |  |
| `attributes.requireDropPoint` | object |  |
| `attributes.returnAddressId` | object |  |
| `attributes.senderAddressId` | object |  |
| `attributes.shadowBookingKeepDocuments` | object |  |
| `attributes.shadowBookingKeepLabels` | object |  |
| `attributes.updatedAt` | string |  |
| `attributes.visibleFor` | object |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.copyright` | string |  |
| `relationships.carrier.links.related` | string |  |
| `relationships.carrier.links.self` | string |  |
| `relationships.documentTemplate.data` | object |  |
| `relationships.documentTemplate.links.related` | string |  |
| `relationships.documentTemplate.links.self` | string |  |
| `relationships.mailTemplate.data` | object |  |
| `relationships.mailTemplate.links.related` | string |  |
| `relationships.mailTemplate.links.self` | string |  |
| `relationships.orderChannel.links.related` | string |  |
| `relationships.orderChannel.links.self` | string |  |
| `relationships.regions.links.related` | string |  |
| `relationships.regions.links.self` | string |  |
| `relationships.returnAddress.links.related` | string |  |
| `relationships.returnAddress.links.self` | string |  |
| `relationships.returnMailTemplate.data` | object |  |
| `relationships.returnMailTemplate.links.related` | string |  |
| `relationships.returnMailTemplate.links.self` | string |  |
| `relationships.returnShippingRate.links.related` | string |  |
| `relationships.returnShippingRate.links.self` | string |  |
| `relationships.senderAddress.links.related` | string |  |
| `relationships.senderAddress.links.self` | string |  |
| `relationships.shadowBookingShippingRate.links.related` | string |  |
| `relationships.shadowBookingShippingRate.links.self` | string |  |
| `relationships.stores.links.related` | string |  |
| `relationships.stores.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `POST /shipping_rates` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipping-rate.md) for the provider-specific parameters and requirements.

