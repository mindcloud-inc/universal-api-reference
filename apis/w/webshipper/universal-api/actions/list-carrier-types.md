# Webshipper: List Carrier Types

Retrieves carrier types from Webshipper.

```
GET https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-carrier-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-carrier-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-carrier-types?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
        "barcodeCustomerNotificationMailTemplateId": {},
        "barcodeMail": {},
        "beta": true,
        "carrierCode": "string",
        "carrierGroupId": "string",
        "colliTypeSupport": {},
        "description": "string",
        "fulfillmentLogo": "string",
        "hide": true,
        "isEdi": true,
        "listLogo": "string",
        "name": "Ava Chen",
        "onboardingUrl": "https://example.com",
        "rateQuoteValidation": true,
        "requiredDetails": "string",
        "requireFtpConfigurationId": true,
        "requiresApproval": true,
        "requiresDutiable": {},
        "shipmentUpdatesLimitMinutes": 1,
        "showSendTime": {},
        "supportsDeletion": true,
        "supportsDocuments": true,
        "supportsPickup": true,
        "supportsPricePdfUpload": true,
        "supportsPriceQuoting": {},
        "supportsShadowBookings": true,
        "supportsShipmentUpdates": true,
        "supportsTestMode": true,
        "supportsTracking": true,
        "supportsZpl": {}
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "copyright": "string"
      },
      "relationships": {
        "carriers": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.barcodeCustomerNotificationMailTemplateId` | object |  |
| `attributes.barcodeMail` | object |  |
| `attributes.beta` | boolean |  |
| `attributes.carrierCode` | string |  |
| `attributes.carrierGroupId` | string |  |
| `attributes.colliTypeSupport` | object |  |
| `attributes.description` | string |  |
| `attributes.fulfillmentLogo` | string |  |
| `attributes.hide` | boolean |  |
| `attributes.isEdi` | boolean |  |
| `attributes.listLogo` | string |  |
| `attributes.name` | string |  |
| `attributes.onboardingUrl` | string |  |
| `attributes.rateQuoteValidation` | boolean |  |
| `attributes.requiredDetails` | string |  |
| `attributes.requireFtpConfigurationId` | boolean |  |
| `attributes.requiresApproval` | boolean |  |
| `attributes.requiresDutiable` | object |  |
| `attributes.shipmentUpdatesLimitMinutes` | number |  |
| `attributes.showSendTime` | object |  |
| `attributes.supportsDeletion` | boolean |  |
| `attributes.supportsDocuments` | boolean |  |
| `attributes.supportsPickup` | boolean |  |
| `attributes.supportsPricePdfUpload` | boolean |  |
| `attributes.supportsPriceQuoting` | object |  |
| `attributes.supportsShadowBookings` | boolean |  |
| `attributes.supportsShipmentUpdates` | boolean |  |
| `attributes.supportsTestMode` | boolean |  |
| `attributes.supportsTracking` | boolean |  |
| `attributes.supportsZpl` | object |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.copyright` | string |  |
| `relationships.carriers.links.related` | string |  |
| `relationships.carriers.links.self` | string |  |
| `relationships.localAttrs.links.related` | string |  |
| `relationships.localAttrs.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `GET /carrier_types` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-carrier-types.md) for the provider-specific parameters and requirements.

