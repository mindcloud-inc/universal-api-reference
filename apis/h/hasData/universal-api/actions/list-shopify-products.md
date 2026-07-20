# HasData: List Shopify Products

Retrieves Shopify products from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-shopify-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-shopify-products?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/list-shopify-products?${params}`, {
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
| `collection` | string | no | Collection handle to filter products. |
| `limit` | number | no | Maximum number of products to retrieve. |
| `page` | number | no | Page number of product results. |
| `url` | string | yes | Shopify store URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "products": [
        {}
      ],
      "requestMetadata": {
        "id": "string",
        "json": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `products` | array<object> | Shopify products returned for the store query. |
| `requestMetadata.id` | string | HasData request identifier. |
| `requestMetadata.json` | string | URL to the JSON payload file. |
| `requestMetadata.status` | string | Request status returned by HasData. |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/shopify/products` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shopify-products.md) for the provider-specific parameters and requirements.

