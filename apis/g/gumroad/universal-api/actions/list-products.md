# Gumroad: List Products

Retrieves products from Gumroad.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/list-products?${params}`, {
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
      "products": [
        [
          {}
        ]
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `products[]` | array<object> |  |
| `products[].currency` | string |  |
| `products[].customDeliveryUrl` | string |  |
| `products[].customFields[]` | array<object> |  |
| `products[].customizablePrice` | boolean |  |
| `products[].customPermalink` | string |  |
| `products[].customReceipt` | string |  |
| `products[].customSummary` | string |  |
| `products[].deleted` | boolean |  |
| `products[].description` | string |  |
| `products[].fileInfo` | object |  |
| `products[].formattedPrice` | string |  |
| `products[].id` | string |  |
| `products[].isTieredMembership` | boolean |  |
| `products[].maxPurchaseCount` | number |  |
| `products[].name` | string |  |
| `products[].previewUrl` | string |  |
| `products[].price` | number |  |
| `products[].published` | boolean |  |
| `products[].purchasingPowerParityPrices` | object |  |
| `products[].recurrences[]` | array<string> |  |
| `products[].requireShipping` | boolean |  |
| `products[].salesCount` | number |  |
| `products[].salesUsdCents` | number |  |
| `products[].shortUrl` | string |  |
| `products[].subscriptionDuration` | string |  |
| `products[].tags[]` | array<string> |  |
| `products[].thumbnailUrl` | string |  |
| `products[].url` | string |  |
| `products[].variants[]` | array<object> |  |
| `products[].variants[].options[]` | array<object> |  |
| `products[].variants[].options[].isPayWhatYouWant` | boolean |  |
| `products[].variants[].options[].name` | string |  |
| `products[].variants[].options[].priceDifference` | number |  |
| `products[].variants[].options[].purchasingPowerParityPrices` | object |  |
| `products[].variants[].options[].recurrencePrices` | object |  |
| `products[].variants[].title` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `GET /products` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

