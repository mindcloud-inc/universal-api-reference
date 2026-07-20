# Gumroad: Get Product

Retrieves a product from Gumroad.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-product?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-product?${params}`, {
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
| `id` | string | yes | The product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "product": {
        "currency": "string",
        "customDeliveryUrl": "https://example.com",
        "customFields": [
          [
            {}
          ]
        ],
        "customizablePrice": true,
        "customPermalink": "https://example.com",
        "customReceipt": "string",
        "customSummary": "string",
        "deleted": true,
        "description": "string",
        "fileInfo": {},
        "formattedPrice": "string",
        "id": "string",
        "isTieredMembership": true,
        "maxPurchaseCount": 1,
        "name": "Ava Chen",
        "previewUrl": "https://example.com",
        "price": 1,
        "published": true,
        "purchasingPowerParityPrices": {},
        "recurrences": [
          [
            "string"
          ]
        ],
        "requireShipping": true,
        "salesCount": 1,
        "salesUsdCents": 1,
        "shortUrl": "https://example.com",
        "subscriptionDuration": "string",
        "tags": [
          [
            "string"
          ]
        ],
        "thumbnailUrl": "https://example.com",
        "url": "https://example.com",
        "variants": [
          [
            {}
          ]
        ]
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `product` | object |  |
| `product.currency` | string |  |
| `product.customDeliveryUrl` | string |  |
| `product.customFields[]` | array<object> |  |
| `product.customizablePrice` | boolean |  |
| `product.customPermalink` | string |  |
| `product.customReceipt` | string |  |
| `product.customSummary` | string |  |
| `product.deleted` | boolean |  |
| `product.description` | string |  |
| `product.fileInfo` | object |  |
| `product.formattedPrice` | string |  |
| `product.id` | string |  |
| `product.isTieredMembership` | boolean |  |
| `product.maxPurchaseCount` | number |  |
| `product.name` | string |  |
| `product.previewUrl` | string |  |
| `product.price` | number |  |
| `product.published` | boolean |  |
| `product.purchasingPowerParityPrices` | object |  |
| `product.recurrences[]` | array<string> |  |
| `product.requireShipping` | boolean |  |
| `product.salesCount` | number |  |
| `product.salesUsdCents` | number |  |
| `product.shortUrl` | string |  |
| `product.subscriptionDuration` | string |  |
| `product.tags[]` | array<string> |  |
| `product.thumbnailUrl` | string |  |
| `product.url` | string |  |
| `product.variants[]` | array<object> |  |
| `product.variants[].options[]` | array<object> |  |
| `product.variants[].options[].isPayWhatYouWant` | boolean |  |
| `product.variants[].options[].name` | string |  |
| `product.variants[].options[].priceDifference` | number |  |
| `product.variants[].options[].purchasingPowerParityPrices` | object |  |
| `product.variants[].options[].recurrencePrices` | object |  |
| `product.variants[].title` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `GET /products/:id` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

