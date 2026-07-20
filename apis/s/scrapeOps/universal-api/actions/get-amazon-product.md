# ScrapeOps: Get Amazon Product

Retrieves Amazon product data from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-amazon-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-amazon-product?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-amazon-product?${params}`, {
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
| `asin` | string | no | Amazon ASIN for the product to fetch. |
| `url` | string | no | Full Amazon product URL to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability_status": "string",
      "average_rating": 1,
      "brand": "string",
      "brand_url": "https://example.com",
      "feature_bullets": [
        [
          "string"
        ]
      ],
      "full_description": "string",
      "images": [
        [
          "string"
        ]
      ],
      "list_price": "string",
      "name": "Ava Chen",
      "pricing": "string",
      "product_category": "string",
      "product_information": {
        "ASIN": "string"
      },
      "shipping_price": "string",
      "shipping_time": "string",
      "ships_from": "string",
      "sold_by": "string",
      "total_ratings": 1,
      "total_reviews": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability_status` | string | Availability status. |
| `average_rating` | number | Average rating. |
| `brand` | string | Brand name. |
| `brand_url` | string | Brand URL. |
| `feature_bullets[]` | array<string> | Feature bullet points. |
| `full_description` | string | Full product description. |
| `images[]` | array<string> | Product image URLs. |
| `list_price` | string | List price text. |
| `name` | string | Product name. |
| `pricing` | string | Current price text. |
| `product_category` | string | Product category. |
| `product_information.ASIN` | string | Amazon ASIN. |
| `shipping_price` | string | Shipping price text. |
| `shipping_time` | string | Shipping time text. |
| `ships_from` | string | Ships from. |
| `sold_by` | string | Sold by. |
| `total_ratings` | number | Total ratings. |
| `total_reviews` | number | Total reviews. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/amazon/product` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-amazon-product.md) for the provider-specific parameters and requirements.

