# Rakuten Advertising: Search products

Finds products in Rakuten Advertising by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/search-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/search-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/search-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "mid": "string",
      "name": "Ava Chen",
      "price": 1,
      "rawXml": "string",
      "sku": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `mid` | string |  |
| `name` | string |  |
| `price` | number |  |
| `rawXml` | string |  |
| `sku` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /productsearch/1.0` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-products.md) for the provider-specific parameters and requirements.

