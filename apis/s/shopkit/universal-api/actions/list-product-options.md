# Shopkit: List Product Options

Retrieves product options from Shopkit.

```
GET https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-product-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-product-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-product-options?${params}`, {
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
      "active": true,
      "barcode": "string",
      "id": 1,
      "id_variant_1": 1,
      "id_variant_2": 1,
      "image": {},
      "price": 1,
      "reference": "string",
      "stock": 1,
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `barcode` | string |  |
| `id` | number |  |
| `id_variant_1` | number |  |
| `id_variant_2` | number |  |
| `image` | object |  |
| `price` | number |  |
| `reference` | string |  |
| `stock` | number |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Shopkit API, this operation is `GET /product/:id/option` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-product-options.md) for the provider-specific parameters and requirements.

