# ScrapingDog: Get Amazon Product

Retrieves Amazon product details through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-amazon-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-amazon-product?connectionId=$CONNECTION_ID&asin=string&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asin": "string",
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-amazon-product?${params}`, {
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
| `asin` | string | yes | Amazon product identifier. |
| `country` | string | no | Target Amazon country code. Default: `us`. |
| `domain` | string | yes | Amazon top-level domain. |

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
      "customization_options": {
        "color": [
          "string"
        ],
        "size": [
          "string"
        ],
        "style": [
          "string"
        ]
      },
      "description": "string",
      "feature_bullets": [
        "string"
      ],
      "images": [
        "string"
      ],
      "list_price": "string",
      "merchant_info": "string",
      "number_of_videos": 1,
      "other_sellers": [
        "string"
      ],
      "price": "string",
      "product_category": "string",
      "product_information": {
        "ASINundefined": "string",
        "CustomerReviews": "string",
        "UPCundefined": "string"
      },
      "shipping_info": "string",
      "ships_from": "string",
      "sold_by": "string",
      "title": "string",
      "total_answered_questions": "string",
      "total_reviews": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability_status` | string |  |
| `average_rating` | number |  |
| `brand` | string |  |
| `brand_url` | string |  |
| `customization_options` | object |  |
| `customization_options.color` | array<string> |  |
| `customization_options.size` | array<string> |  |
| `customization_options.style` | array<string> |  |
| `description` | string |  |
| `feature_bullets` | array<string> |  |
| `images` | array<string> |  |
| `list_price` | string |  |
| `merchant_info` | string |  |
| `number_of_videos` | number |  |
| `other_sellers` | array<string> |  |
| `price` | string |  |
| `product_category` | string |  |
| `product_information` | object |  |
| `product_information.ASINundefined` | string |  |
| `product_information.CustomerReviews` | string |  |
| `product_information.UPCundefined` | string |  |
| `shipping_info` | string |  |
| `ships_from` | string |  |
| `sold_by` | string |  |
| `title` | string |  |
| `total_answered_questions` | string |  |
| `total_reviews` | number |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /amazon/product` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-amazon-product.md) for the provider-specific parameters and requirements.

