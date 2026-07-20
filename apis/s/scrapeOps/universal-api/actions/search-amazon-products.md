# ScrapeOps: Search Amazon Products

Retrieves Amazon search results from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-amazon-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-amazon-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/search-amazon-products?${params}`, {
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
| `query` | string | no | Amazon search query. |
| `url` | string | no | Full Amazon search URL to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asin": "string",
      "badge": "string",
      "image": "string",
      "name": "Ava Chen",
      "original_price": 1,
      "price": 1,
      "shipping": "string",
      "stars": 1,
      "total_reviews": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asin` | string | Amazon ASIN. |
| `badge` | string | Product badge. |
| `image` | string | Product image URL. |
| `name` | string | Product name. |
| `original_price` | number | Original price. |
| `price` | number | Current price. |
| `shipping` | string | Shipping text. |
| `stars` | number | Average star rating. |
| `total_reviews` | number | Total reviews. |
| `url` | string | Product URL. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/amazon/search` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-amazon-products.md) for the provider-specific parameters and requirements.

