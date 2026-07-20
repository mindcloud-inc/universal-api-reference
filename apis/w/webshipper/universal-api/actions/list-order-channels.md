# Webshipper: List Order Channels

Retrieves order channels from Webshipper.

```
GET https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-order-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-order-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-order-channels?${params}`, {
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
        "additionalParameters": {},
        "autoOrderImport": true,
        "channelLabel": "string",
        "configurationToken": {},
        "convertCurrencyOnRateQuotes": {},
        "createShipmentAutomatically": true,
        "documentPrintMode": "string",
        "dropPointLimit": 1,
        "failedSyncCount": 1,
        "fulfillAutomatically": true,
        "hasConfigurationToken": true,
        "health": {
          "health": 1,
          "health1d": 1,
          "health1h": 1,
          "health1w": 1
        },
        "logo": {},
        "returnLabelPrintMode": "string",
        "shippingLabelPrintMode": "string",
        "slipPrintMode": "string",
        "syncAdditionalAttributesToShipments": true,
        "syncStatus": "string"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "copyright": "string"
      },
      "relationships": {
        "additionalAttributes": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "defaultPrinterClient": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "orderChannelSyncEntries": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "orderChannelType": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "orders": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "pickupAddress": {
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
        "senderAddress": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "shippingMappings": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "shippingRates": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "slipTemplate": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "soldFromAddress": {
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
| `attributes.additionalParameters` | object |  |
| `attributes.autoOrderImport` | boolean |  |
| `attributes.channelLabel` | string |  |
| `attributes.configurationToken` | object |  |
| `attributes.convertCurrencyOnRateQuotes` | object |  |
| `attributes.createShipmentAutomatically` | boolean |  |
| `attributes.documentPrintMode` | string |  |
| `attributes.dropPointLimit` | number |  |
| `attributes.failedSyncCount` | number |  |
| `attributes.fulfillAutomatically` | boolean |  |
| `attributes.hasConfigurationToken` | boolean |  |
| `attributes.health.health` | number |  |
| `attributes.health.health1d` | number |  |
| `attributes.health.health1h` | number |  |
| `attributes.health.health1w` | number |  |
| `attributes.logo` | object |  |
| `attributes.returnLabelPrintMode` | string |  |
| `attributes.shippingLabelPrintMode` | string |  |
| `attributes.slipPrintMode` | string |  |
| `attributes.syncAdditionalAttributesToShipments` | boolean |  |
| `attributes.syncStatus` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.copyright` | string |  |
| `relationships.additionalAttributes.links.related` | string |  |
| `relationships.additionalAttributes.links.self` | string |  |
| `relationships.defaultPrinterClient.links.related` | string |  |
| `relationships.defaultPrinterClient.links.self` | string |  |
| `relationships.orderChannelSyncEntries.links.related` | string |  |
| `relationships.orderChannelSyncEntries.links.self` | string |  |
| `relationships.orderChannelType.links.related` | string |  |
| `relationships.orderChannelType.links.self` | string |  |
| `relationships.orders.links.related` | string |  |
| `relationships.orders.links.self` | string |  |
| `relationships.pickupAddress.links.related` | string |  |
| `relationships.pickupAddress.links.self` | string |  |
| `relationships.returnAddress.links.related` | string |  |
| `relationships.returnAddress.links.self` | string |  |
| `relationships.senderAddress.links.related` | string |  |
| `relationships.senderAddress.links.self` | string |  |
| `relationships.shippingMappings.links.related` | string |  |
| `relationships.shippingMappings.links.self` | string |  |
| `relationships.shippingRates.links.related` | string |  |
| `relationships.shippingRates.links.self` | string |  |
| `relationships.slipTemplate.links.related` | string |  |
| `relationships.slipTemplate.links.self` | string |  |
| `relationships.soldFromAddress.links.related` | string |  |
| `relationships.soldFromAddress.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `GET /order_channels` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-channels.md) for the provider-specific parameters and requirements.

