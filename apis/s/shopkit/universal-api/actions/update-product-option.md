# Shopkit: Update Product Option

Updates an existing product option in Shopkit.

```
PUT https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-product-option
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-product-option" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-product-option', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Shopkit API, this operation is `PUT /product/:id/option/:id_option` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-option.md) for the provider-specific parameters and requirements.

