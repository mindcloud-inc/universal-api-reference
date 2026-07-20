# ScrapeOps: Get Walmart Product

Retrieves Walmart product data from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-walmart-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-walmart-product?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-walmart-product?${params}`, {
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
| `country` | string | no | The 2-letter country code to scrape Walmart product data from. |
| `productId` | string | no | Walmart product ID to fetch. |
| `tld` | string | no |  |
| `url` | string | no | Full Walmart product URL to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {
        "about_product": "string",
        "brand": "string",
        "name": "Ava Chen",
        "rating": 1,
        "review_count": "string"
      },
      "images": {
        "main_image": {
          "url": "https://example.com"
        },
        "total_count": 1
      },
      "reviews": {
        "num_reviews": "string",
        "overall_rating": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details.about_product` | string | About product text. |
| `details.brand` | string | Brand name. |
| `details.name` | string | Product name. |
| `details.rating` | number | Rating value. |
| `details.review_count` | string | Review count. |
| `images.main_image.url` | string | Main image URL. |
| `images.total_count` | number | Image count. |
| `reviews.num_reviews` | string | Number of reviews. |
| `reviews.overall_rating` | string | Overall review rating. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/walmart/product` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-walmart-product.md) for the provider-specific parameters and requirements.

