# ScrapeOps: Get Ebay Product

Retrieves eBay product data from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-ebay-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-ebay-product?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-ebay-product?${params}`, {
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
| `itemId` | string | no | eBay item ID to fetch. |
| `url` | string | no | Full eBay product URL to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "images": [
        [
          "string"
        ]
      ],
      "itemSpecifics": {
        "Brand": "string"
      },
      "name": "Ava Chen",
      "price": "string",
      "product_summary": {
        "condition": "string",
        "price_primary": "string",
        "seller_name": "Ava Chen",
        "seller_url": "https://example.com"
      },
      "store_information": {
        "name": "Ava Chen",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `images[]` | array<string> | Product image URLs. |
| `itemSpecifics.Brand` | string | Brand. |
| `name` | string | Product name. |
| `price` | string | Price text. |
| `product_summary.condition` | string | Product condition. |
| `product_summary.price_primary` | string | Primary price text. |
| `product_summary.seller_name` | string | Seller name. |
| `product_summary.seller_url` | string | Seller URL. |
| `store_information.name` | string | Store name. |
| `store_information.url` | string | Store URL. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/ebay/product` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ebay-product.md) for the provider-specific parameters and requirements.

