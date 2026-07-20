# Webshipper: Quote Carrier Services

Creates a carrier service quote in Webshipper.

```
POST https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/quote-carrier-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/quote-carrier-services" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/quote-carrier-services', {
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
        "addOns": {},
        "carrierId": 1,
        "costSheetId": {},
        "deliveryAddress": {
          "address1": "string",
          "city": "string",
          "companyName": "Ava Chen",
          "countryCode": "string",
          "zip": "string"
        },
        "dutiable": {},
        "isReturn": true,
        "packages": [
          {
            "dimensions": {
              "height": 1,
              "length": 1,
              "unit": "string",
              "width": 1
            },
            "weight": 1,
            "weightUnit": "string"
          }
        ],
        "sendDate": "string",
        "senderAddress": {
          "address1": "string",
          "city": "string",
          "companyName": "Ava Chen",
          "countryCode": "string",
          "zip": "string"
        },
        "sendTime": "string",
        "serviceAttributes": {},
        "serviceCode": {},
        "services": [
          {
            "approved": true,
            "barcodeRequirement": {},
            "bookingQuoteInfo": {},
            "carrierLibraryInternals": {},
            "costDetails": {},
            "costPrice": {},
            "countryCombinations": {},
            "currency": {},
            "estimatedDeliveryDateFrom": {},
            "estimatedDeliveryDateTo": {},
            "hidden": {},
            "invoiceSettings": {},
            "isReturn": true,
            "loadMeters": {},
            "requiresApproval": {},
            "requiresDropPoint": true,
            "serviceCode": "string",
            "serviceName": "Ava Chen",
            "shipmentBarcodeRequirement": {},
            "showPickupForm": {},
            "supportsPaperless": true,
            "usingCostSheet": {},
            "vatPercent": {},
            "volume": {},
            "waybillRequirement": {}
          }
        ],
        "success": true,
        "timeout": {}
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "copyright": "string"
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
| `attributes.addOns` | object |  |
| `attributes.carrierId` | number |  |
| `attributes.costSheetId` | object |  |
| `attributes.deliveryAddress.address1` | string |  |
| `attributes.deliveryAddress.city` | string |  |
| `attributes.deliveryAddress.companyName` | string |  |
| `attributes.deliveryAddress.countryCode` | string |  |
| `attributes.deliveryAddress.zip` | string |  |
| `attributes.dutiable` | object |  |
| `attributes.isReturn` | boolean |  |
| `attributes.packages[].dimensions.height` | number |  |
| `attributes.packages[].dimensions.length` | number |  |
| `attributes.packages[].dimensions.unit` | string |  |
| `attributes.packages[].dimensions.width` | number |  |
| `attributes.packages[].weight` | number |  |
| `attributes.packages[].weightUnit` | string |  |
| `attributes.sendDate` | string |  |
| `attributes.senderAddress.address1` | string |  |
| `attributes.senderAddress.city` | string |  |
| `attributes.senderAddress.companyName` | string |  |
| `attributes.senderAddress.countryCode` | string |  |
| `attributes.senderAddress.zip` | string |  |
| `attributes.sendTime` | string |  |
| `attributes.serviceAttributes` | object |  |
| `attributes.serviceCode` | object |  |
| `attributes.services[].approved` | boolean |  |
| `attributes.services[].barcodeRequirement` | object |  |
| `attributes.services[].bookingQuoteInfo` | object |  |
| `attributes.services[].carrierLibraryInternals` | object |  |
| `attributes.services[].costDetails` | object |  |
| `attributes.services[].costPrice` | object |  |
| `attributes.services[].countryCombinations` | object |  |
| `attributes.services[].currency` | object |  |
| `attributes.services[].estimatedDeliveryDateFrom` | object |  |
| `attributes.services[].estimatedDeliveryDateTo` | object |  |
| `attributes.services[].hidden` | object |  |
| `attributes.services[].invoiceSettings` | object |  |
| `attributes.services[].isReturn` | boolean |  |
| `attributes.services[].loadMeters` | object |  |
| `attributes.services[].requiresApproval` | object |  |
| `attributes.services[].requiresDropPoint` | boolean |  |
| `attributes.services[].serviceCode` | string |  |
| `attributes.services[].serviceName` | string |  |
| `attributes.services[].shipmentBarcodeRequirement` | object |  |
| `attributes.services[].showPickupForm` | object |  |
| `attributes.services[].supportsPaperless` | boolean |  |
| `attributes.services[].usingCostSheet` | object |  |
| `attributes.services[].vatPercent` | object |  |
| `attributes.services[].volume` | object |  |
| `attributes.services[].waybillRequirement` | object |  |
| `attributes.success` | boolean |  |
| `attributes.timeout` | object |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.copyright` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `POST /service_quotes` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/quote-carrier-services.md) for the provider-specific parameters and requirements.

