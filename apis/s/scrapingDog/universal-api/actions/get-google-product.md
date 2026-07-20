# ScrapingDog: Get Google Product

Retrieves Google product details through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-product?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-product?${params}`, {
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
| `productId` | string | yes | Google Shopping product ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "online_sellers": {
        "base_price": "string",
        "delivery": "string",
        "link": "https://example.com",
        "name": "Ava Chen",
        "position": 1,
        "total_price": "string"
      },
      "product_results": {
        "conditions": [
          "string"
        ],
        "extensions": [
          "string"
        ],
        "features": [
          "string"
        ],
        "prices": [
          "string"
        ],
        "rating": "string",
        "reviews": "string",
        "title": "string",
        "typical_prices": {
          "high": "string",
          "low": "string",
          "shown_price": "string"
        }
      },
      "product_variations": {
        "thumbnail": "string"
      },
      "related_products": {
        "link": "https://example.com",
        "price": "string",
        "title": "string"
      },
      "reviews_results": {
        "ratings": {
          "amount": "string",
          "name": "Ava Chen"
        },
        "reviews": {
          "date": "string",
          "description": "string",
          "position": 1,
          "rating": "string",
          "source": "string",
          "title": "string"
        }
      },
      "specifications": {
        "details": {
          "Manufacturer Part Number": "string",
          "Phone Style": "string",
          "Product Line": "string",
          "Product Name": "Ava Chen",
          "Product Type": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `online_sellers` | array<object> |  |
| `online_sellers.base_price` | string |  |
| `online_sellers.delivery` | string |  |
| `online_sellers.link` | string |  |
| `online_sellers.name` | string |  |
| `online_sellers.position` | number |  |
| `online_sellers.total_price` | string |  |
| `product_results` | object |  |
| `product_results.conditions` | array<string> |  |
| `product_results.extensions` | array<string> |  |
| `product_results.features` | array<string> |  |
| `product_results.prices` | array<string> |  |
| `product_results.rating` | string |  |
| `product_results.reviews` | string |  |
| `product_results.title` | string |  |
| `product_results.typical_prices` | object |  |
| `product_results.typical_prices.high` | string |  |
| `product_results.typical_prices.low` | string |  |
| `product_results.typical_prices.shown_price` | string |  |
| `product_variations` | array<object> |  |
| `product_variations.thumbnail` | string |  |
| `related_products` | array<object> |  |
| `related_products.link` | string |  |
| `related_products.price` | string |  |
| `related_products.title` | string |  |
| `reviews_results` | object |  |
| `reviews_results.ratings` | array<object> |  |
| `reviews_results.ratings.amount` | string |  |
| `reviews_results.ratings.name` | string |  |
| `reviews_results.reviews` | array<object> |  |
| `reviews_results.reviews.date` | string |  |
| `reviews_results.reviews.description` | string |  |
| `reviews_results.reviews.position` | number |  |
| `reviews_results.reviews.rating` | string |  |
| `reviews_results.reviews.source` | string |  |
| `reviews_results.reviews.title` | string |  |
| `specifications` | object |  |
| `specifications.details` | object |  |
| `specifications.details.Manufacturer Part Number` | string |  |
| `specifications.details.Phone Style` | string |  |
| `specifications.details.Product Line` | string |  |
| `specifications.details.Product Name` | string |  |
| `specifications.details.Product Type` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_product` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-product.md) for the provider-specific parameters and requirements.

