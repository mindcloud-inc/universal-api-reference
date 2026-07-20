# Scrape do: Get Amazon product details

Retrieves Amazon product details with Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-amazon-product-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-amazon-product-details?connectionId=$CONNECTION_ID&asin=string&geocode=string&zipcode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asin": "string",
  "geocode": "string",
  "zipcode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-amazon-product-details?${params}`, {
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
| `asin` | string | yes | The 10-character Amazon product identifier. |
| `geocode` | string | yes | Amazon marketplace country code such as us, gb, de, or jp. |
| `zipcode` | string | yes | Postal code formatted for the selected marketplace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asin": "string",
      "best_seller_rankings": [
        {}
      ],
      "brand": "string",
      "currency": "string",
      "currency_symbol": "string",
      "errorMessage": "string",
      "images": [
        {}
      ],
      "is_prime": true,
      "is_sponsored": true,
      "list_price": 1,
      "more_buying_choices": {},
      "name": "Ava Chen",
      "price": 1,
      "rating": 1,
      "shipping_info": [
        "string"
      ],
      "status": "string",
      "technical_details": {},
      "thumbnail": "string",
      "total_ratings": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asin` | string | Amazon product ASIN. |
| `best_seller_rankings` | array<object> | Best seller ranking entries. |
| `brand` | string | Product brand. |
| `currency` | string | Currency code. |
| `currency_symbol` | string | Currency symbol. |
| `errorMessage` | string | Error text when the request fails. |
| `images` | array<object> | Product image objects. |
| `is_prime` | boolean | Whether Prime shipping is available. |
| `is_sponsored` | boolean | Whether the product is sponsored. |
| `list_price` | number | Original list price when present. |
| `more_buying_choices` | object | Alternative seller information. |
| `name` | string | Full product title. |
| `price` | number | Current product price. |
| `rating` | number | Average product rating. |
| `shipping_info` | array<string> | Shipping information strings. |
| `status` | string | Request status. |
| `technical_details` | object | Technical specification key-value pairs. |
| `thumbnail` | string | Primary product image URL. |
| `total_ratings` | number | Total customer ratings. |
| `url` | string | Canonical product URL. |

## Native endpoint

Through the native Scrape do API, this operation is `GET /plugin/amazon/pdp` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-amazon-product-details.md) for the provider-specific parameters and requirements.

