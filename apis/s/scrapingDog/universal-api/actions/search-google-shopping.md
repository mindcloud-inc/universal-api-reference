# ScrapingDog: Search Google Shopping

Retrieves Google Shopping search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-shopping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-shopping?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-shopping?${params}`, {
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
| `query` | string | yes | Search query for Google Shopping. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": {
        "link": "https://example.com",
        "price": "string",
        "source": "string",
        "thumbnail": "string",
        "title": "string"
      },
      "filters": {
        "options": {
          "tbs": "string",
          "text": "string"
        },
        "type": "string"
      },
      "shopping_results": {
        "extensions": [
          "string"
        ],
        "extracted_price": 1,
        "old_price_extracted": "string",
        "position": 1,
        "price": "string",
        "product_id": "string",
        "product_link": "https://example.com",
        "rating": 1,
        "reviews": "string",
        "scrapingdog_immersive_product_link": "https://example.com",
        "source": "string",
        "thumbnail": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads` | array<object> |  |
| `ads.link` | string |  |
| `ads.price` | string |  |
| `ads.source` | string |  |
| `ads.thumbnail` | string |  |
| `ads.title` | string |  |
| `filters` | array<object> |  |
| `filters.options` | array<object> |  |
| `filters.options.tbs` | string |  |
| `filters.options.text` | string |  |
| `filters.type` | string |  |
| `shopping_results` | array<object> |  |
| `shopping_results.extensions` | array<string> |  |
| `shopping_results.extracted_price` | number |  |
| `shopping_results.old_price_extracted` | string |  |
| `shopping_results.position` | number |  |
| `shopping_results.price` | string |  |
| `shopping_results.product_id` | string |  |
| `shopping_results.product_link` | string |  |
| `shopping_results.rating` | number |  |
| `shopping_results.reviews` | string |  |
| `shopping_results.scrapingdog_immersive_product_link` | string |  |
| `shopping_results.source` | string |  |
| `shopping_results.thumbnail` | string |  |
| `shopping_results.title` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_shopping` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-shopping.md) for the provider-specific parameters and requirements.

