# Webshipper: Quote Order Channel Rates

Creates an order channel rate quote in Webshipper.

```
POST https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/quote-order-channel-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/quote-order-channel-rates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/quote-order-channel-rates', {
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
        "additionalAttributes": {},
        "currency": {},
        "deliveryAddress": {
          "address1": "string",
          "city": "string",
          "companyName": "Ava Chen",
          "countryCode": "string",
          "zip": "string"
        },
        "dimensionsUnit": {},
        "filterByCurrency": {},
        "height": {},
        "includeHidden": {},
        "isReturn": {},
        "items": [
          {
            "description": "string",
            "quantity": 1,
            "sku": "string"
          }
        ],
        "length": {},
        "orderChannelId": 1,
        "price": 1,
        "senderAddress": {},
        "success": true,
        "weight": 1,
        "weightUnit": "string",
        "width": {}
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
| `attributes.additionalAttributes` | object |  |
| `attributes.currency` | object |  |
| `attributes.deliveryAddress.address1` | string |  |
| `attributes.deliveryAddress.city` | string |  |
| `attributes.deliveryAddress.companyName` | string |  |
| `attributes.deliveryAddress.countryCode` | string |  |
| `attributes.deliveryAddress.zip` | string |  |
| `attributes.dimensionsUnit` | object |  |
| `attributes.filterByCurrency` | object |  |
| `attributes.height` | object |  |
| `attributes.includeHidden` | object |  |
| `attributes.isReturn` | object |  |
| `attributes.items[].description` | string |  |
| `attributes.items[].quantity` | number |  |
| `attributes.items[].sku` | string |  |
| `attributes.length` | object |  |
| `attributes.orderChannelId` | number |  |
| `attributes.price` | number |  |
| `attributes.senderAddress` | object |  |
| `attributes.success` | boolean |  |
| `attributes.weight` | number |  |
| `attributes.weightUnit` | string |  |
| `attributes.width` | object |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.copyright` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `POST /rate_quotes` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/quote-order-channel-rates.md) for the provider-specific parameters and requirements.

