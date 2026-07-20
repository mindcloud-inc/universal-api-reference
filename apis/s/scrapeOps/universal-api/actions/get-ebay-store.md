# ScrapeOps: Get Ebay Store

Retrieves eBay store data from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-ebay-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-ebay-store?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/get-ebay-store?${params}`, {
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
| `storeName` | string | no | eBay store name to fetch. |
| `url` | string | no | Full eBay store URL to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "banner": {
        "image": "string"
      },
      "products": {
        "more": "string",
        "products": [
          {
            "name": [
              "Ava Chen"
            ],
            "price": [
              "string"
            ]
          }
        ]
      },
      "seller": {
        "logo": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `banner.image` | string | Banner image URL. |
| `products.more` | string | More products URL. |
| `products.products[].name` | array<string> | Store product names. |
| `products.products[].price` | array<string> | Store product prices. |
| `seller.logo` | string | Seller logo URL. |
| `seller.name` | string | Seller name. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/ebay/store` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ebay-store.md) for the provider-specific parameters and requirements.

